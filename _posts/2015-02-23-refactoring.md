---
layout: post
title: Refactoring Mindset
date: 2015-02-23 2:30PM
---

# SD 5.7 Exercise
**a.** The module in *RMH Homebase* that displays a shift's notes field is the calendar module. 

**b.** Two instances of "ugly code" are as follows:

### calendar.php line 62

{% highlight php startinline %}
if ($edit==true && !($days[6]->get_year()<$year 
    || ($days[6]->get_year()==$year 
    && $days[6]->get_day_of_year()<$doy) ) 
    && $_SESSION['access_level']>=2)
        echo "<p align=\"center\">
        <input type=\"submit\" 
        value=\"Save changes to all notes\" 
        name=\"submit\">";
{% endhighlight %}

### calendarFam.php line 64
{% highlight php startinline %}
if ($edit==true && !($days[6]->get_year()<$year 
    || ($days[6]->get_year()==$year 
    && $days[6]->get_day_of_year()<$doy) ) 
    && $_SESSION['access_level']>=2)
        echo "<p align=\"center\">
        <input type=\"submit\" 
        value=\"Save changes to all notes\" 
        name=\"submit\">";
{% endhighlight %}

Truly awful. Let's fix it!

**c.** To avoid this repetition a function `predates` can be created that will return true or false if `a` predates `b`.

{% highlight php startinline %}
function predates($days,$year,$doy) {
    if !(
        $days[6]->get_year() < $year ||
        ($days[6]->get_year()== $year &&
        $days[6]->get_day_of_year()<$doy)
    ) { 
        return True; 
    }
    else { 
        return False; 
    }
}
{% endhighlight %}

**d.** Now the long if statement can be replaced as follows:
{% highlight php startinline %}
if( $edit==true && predates($days,$year,$doy) 
    && $_SESSION['access_level']>=2)
        ...
{% endhighlight %}

# SD 5.8 Exercise
**a.** Looking at **editShift.php lines 60-74:**
{% highlight php startinline %}
if($shift->num_vacancies()>0) {
    echo("<tr><td valign=\"top\">
    <br>&nbsp;Find Volunteers
    <br>&nbsp;To Fill Vacancies</td>
    <td>
    <form method=\"POST\" action=\"subCallList.php\" 
    style=\"margin-bottom:0;\">
    <input type=\"hidden\" name=\"_shiftid\" 
    value=\"".$shiftid."\">");
    if(!$shift->has_sub_call_list() || 
        !(select_dbSCL($shift->get_id()) instanceof SCL)) {
            echo "<input type=\"hidden\" 
            name=\"_submit_generate_scl\" value=\"1\"><br>
            <input type=\"submit\" 
            value=\"Generate Sub Call List\" 
            name=\"submit\" style=\"width: 250px\">";
    }
    else {
        echo "<input type=\"hidden\" 
        name=\"_submit_view_scl\" value=\"1\"><br>
        <input type=\"submit\" 
        value=\"View Sub Call List\" 
        name=\"submit\" style=\"width: 250px\">";
    }
    echo "</form><br></td></tr>";
}
{% endhighlight %}

We can see that if a shift does *not* have a "sub call list" and there is no instance of a sub call list (SCL) id in the database, then a "Generate Sub Call List" button is created. Otherwise the "View Sub Call List" button is created.

It appears that every shift *can* have a sub call list, but it is optional.

**b.** It would seem that a week is automatically archived.
**addWeek_newweek.inc line 118:**
{% highlight php startinline %}
if($status=="archived") {
    $options="archived (<a href=\"calendar.php?id=
        ".$week[0]."\">view</a>)";
    if ($remove)
       $options = $options . " 
       (<a href=\"addWeek.php?remove=
            ".$week[0]."\">remove</a>)";
    }
else if (time()>$end) {
    $options="archived 
        (<a href=\"calendar.php?id=
            ".$week[0]."\">view</a>)";
    $week2=get_dbWeeks($week[0]);
    $week2->set_status("archived");
    update_dbWeeks($week2);
}
{% endhighlight %}

This is the only instance of code I found in which `set_status("archived");` is called. `$end` is defined here as `$end=$week[7];`. Therefore if the current time is past the end of the week, the status will be set to archived.

Additionally if a week is flagged as archived it will be flagged for removal from the database or have the option to be removed by an administrator. 

While automatic archiving may be useful for some, it can quickly clog a database, especially if removal of those archived weeks is only managed by an administrator. It may be better to have an option to archive weeks, so that those weeks of significance can be stored for future reference, while the usual weeks can simply be removed. 


