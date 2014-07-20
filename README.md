jquery-handler-toolkit.js
=========================

Test if event handler is bound to an element in jQuery (1 or many) - and list event handlers



Original code for listHandlers() comes from: http://james.padolsey.com/javascript/debug-jquery-events-with-listhandlers/

Sample calls for listHandlers :

 $('*').listHandlers('*')
 $('a').listHandlers('onclick')
 or
 if( $('a').listHandlers('onclick')) { ... }
 
 
 
Samples for HasHandlers():

Tells if node with selector '.container-fluid' has any event handler:

  $('.container-fluid').hasHandlers('*')

--> true or false

Check if node with selector '.container-fluid' has 'click' event handler:
  
  $('.container-fluid').hasHandlers('click')
  
--> false

Add an event handler 

$('.container-fluid').on('click', function(){});

  $('.container-fluid').hasHandlers('click')
  
--> true

Other examples: 
  
  $('.scroll').hasHandlers('mouseout')
  
if you use event delegation, meaning for example $('#main').delegate('.adv-search', 'click', function() {}) instead of par  $('.adv-search').click(function() { }), you can still test event handler presence by adding the selector:  

  $('#main').hasHandlers('click','.simple-search')
  
  
  



