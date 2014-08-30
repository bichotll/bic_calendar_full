BIC Calendar
============

ca - BIC Calendar es un simple calendari per marcar esdeveniments. Un plugin de jQuery i Twitter Bootstrap.

en - BIC Calendar is a simple calendar to mark events, a jQuery plugin and Twitter Bootstrap.


Dependencias
------------

- ~jQuery 1.7.2
- ~Twitter Bootstrap 2.0


Options
-------

- popoverOptions (popover Twitter Bootstrap object)

- tooltipOptions (tooltip Twitter Bootstrap object)

- dayNames (array)
    - default: ["l", "m", "x", "j", "v", "s", "d"]

- monthNames (array)
    - default: ["Enero", "Febrero", "Marzo", "Abril", "Mayo", "Junio", "Julio", "Agosto", "Septiembre", "Octubre", "Noviembre", "Diciembre"]

- showDays (boolean)
    - default: true

- reqAjax (json array of event array)
    - reqAjax.type (string) {'get', 'post'}
    - reqAjax.url (string)

- events (array of event array)
    - ex:
```js
    var events = [
        {
            date: "28/10/2013",
            title: 'SPORT & WELLNESS',
            link: '',
            color: '',
            content: '<img src="http://gettingcontacts.com/upload/jornadas/sport-wellness_portada.png" ><br>06-11-2013 - 09:00 <br> Tecnocampus Mataró Auditori',
            class: '',
        }
    ];
```


Use example for the calendar
----------------------------

```js
$(document).ready(function() {

    var monthNames = ["Gener", "Febrer", "Març", "Abril", "Maig", "Juny", "Juliol", "Agost", "Setembre", "Octubre", "Novembre", "Dicembre"];

    var dayNames = ["L", "M", "M", "J", "V", "S", "D"];

    var events = [
        {
            date: "28/10/2013",
            title: 'SPORT & WELLNESS',
            link: '',
            color: '',
            content: '<img src="http://gettingcontacts.com/upload/jornadas/sport-wellness_portada.png" ><br>06-11-2013 - 09:00 <br> Tecnocampus Mataró Auditori',
            class: '',
        }
    ];

    $('#calendari_lateral1').bic_calendar({
        //list of events in array
        events: events,
        //enable select
        enableSelect: true,
        //enable multi-select
        multiSelect: true,
        //set day names
        dayNames: dayNames,
        //set month names
        monthNames: monthNames,
        //show dayNames
        showDays: true,
        //set ajax call
        reqAjax: {
            type: 'get',
            url: 'http://bic.cat/bic_calendar/index.php'
        }
        //set popover options
        //popoverOptions: {}
        //set tooltip options
        //tooltipOptions: {}
    });
});
```


Use example for the calendar events
-----------------------------------
```js
$(document).ready(function() {
    document.addEventListener('bicCalendarSelect', function(e) {
        alert('Hi dude! You selected from ' + e.detail.dateFirst + 'to' + e.detail.dateLast + '. Do whatever you want with these dates.');

        //maybe you would like to send these data by ajax...
        //$.ajax...

        //or asign to a form...
        //$('input').val(...
    });
});
```


TODO
----
    - Clear documentation
    - Add all options


More info
---------
This is just an improved fork of [http://bic.cat/bic_calendar](http://bic.cat/bic_calendar). 
For more info you could check it and its branches.


About IE8
---------
[https://github.com/bichotll/bic_calendar_full/issues/1](https://github.com/bichotll/bic_calendar_full/issues/1)


Other Bic Calendar Full branches
---------
Fully working example for a school calendar. Not so good code, but it does its job.
[https://github.com/bichotll/bic_calendar_full/tree/school](https://github.com/bichotll/bic_calendar_full/tree/school)


Showcase
--------
[http://bic.cat/bic_calendar_full](http://bic.cat/bic_calendar_full)
