---
title: locale
---

Customize the language and localization options for the calendar.

<div class='spec' markdown='1'>
A String locale code. *default*: `"en"`
</div>

This option affects many things such as:

- the text in buttons, as defined by [header](header)
- text that contains month or day-of-week strings
- date formatting, such as [eventTimeFormat](eventTimeFormat)
- [weekNumberCalculation](weekNumberCalculation)
- [firstDay](firstDay)


## How to use other locales

You will need to load the locale JavaScript data file in order to use it.
These files are included with the FullCalendar download in the `locales/` directory.
They must be loaded via a `<script>` tag after the main FullCalendar library is loaded.
TODO

```html
<script src='fullcalendar/fullcalendar.js'></script>
<script src='fullcalendar/locales/es.js'></script>
<script>

  document.addEventListener('DOMContentLoaded', function() {
    var calendarEl = document.getElementById('calendar');

    var calendar = new FullCalendar.Calendar(calendarEl, {
    });

    calendar.render();
  });

</script>
```

If you are simply loading one locale, you do *not* need to specify the `locale` option. FullCalendar will look at the most recent locale file loaded and use it.

However, if more than one locale file is loaded, or the combined `locales-all.js` file is loaded, you must explicitly specify which locale to use via the `locale` option:

```html
<script src='fullcalendar/fullcalendar.js'></script>
<script src='fullcalendar/locales-all.js'></script>
<script>

  document.addEventListener('DOMContentLoaded', function() {
    var calendarEl = document.getElementById('calendar');

    var calendar = new FullCalendar.Calendar(calendarEl, {
      locale: 'es'
    });

    calendar.render();
  });

</script>
```

For more information, [view a live demo](locale-demo).
