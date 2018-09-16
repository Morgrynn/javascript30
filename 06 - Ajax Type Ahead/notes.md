#Ajax Type Ahead

Notes on what I have learned.

1. TypeError: x is null, can't access property "prop" of it

    This was a pretty annoying little problem but eventualy I resolved it.

    Code is basically run from the top to bottom. Most devs put their JavaScript in the head of 
    their HTML file. The Browser has recieved to HTML, CSS and JavaScript from the server; is
    'executing'/rendering the Web page; and is executing the JavaScript, but it hasn't gotten 
    further down the HTML file to 'execute'/render the HTML and fires the event *DOM ready.*

    With raw JavaScript, use window.onload:

```
window.onload=function() {
    /*your code here*/
    /*var date = document.getElementById("date");
    /*alert(date);
} 

```

 This way, your JavaScript won't run until the browser has built the DOM, the HTML element exists (not null :-) ) and your JavaScript can find it and attach an event handler to it.

--Andrew Koper