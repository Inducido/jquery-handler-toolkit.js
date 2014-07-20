jquery-handler-toolkit.js
=========================

Test if event handler is bound to an element in jQuery (1 or many) - and list event handlers


**Work with jQuery v1.11.0**


Original code for listHandlers() comes from: http://james.padolsey.com/javascript/debug-jquery-events-with-listhandlers/

Sample calls for listHandlers
-----------------------------

```js
 $('*').listHandlers('*')
 $('a').listHandlers('onclick')
 or
 if( $('a').listHandlers('onclick')) { ... }
```
 
 
Samples for HasHandlers()
-------------------------

Tells if node with selector '.container-fluid' has any event handler:
```js
  $('.container-fluid').hasHandlers('*')

--> true or false
```

Check if node with selector '.container-fluid' has 'click' event handler:
```js  
  $('.container-fluid').hasHandlers('click')
  
--> false
```

if you add an event handler like the following 
```js
  $('.container-fluid').on('click', function(){});
then 
  $('.container-fluid').hasHandlers('click')
  
--> true
```
Other example in the case of event delegation
---------------------------------------------

```js  
  $('.scroll').hasHandlers('mouseout')
```
if you use event delegation, meaning for example $('#main').delegate('.adv-search', 'click', function() {}) instead of par  $('.adv-search').click(function() { }), you can still test event handler presence by adding the selector:  

```js  
  $('#main').hasHandlers('click','.simple-search')
```  
  
  



