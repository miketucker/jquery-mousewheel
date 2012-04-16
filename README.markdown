# jQuery Mouse Wheel Plugin

A jQuery plugin that adds cross-browser mouse wheel support.

In order to use the plugin, simply bind the "mousewheel" event to an element. It also provides two helper methods called `mousewheel` and `unmousewheel` that act just like other event helper methods in jQuery. The event callback receives three extra arguments which are the normalized "deltas" of the mouse wheel. 

Here is an example of using both the bind and helper method syntax.

    // using bind
    $('#my_elem').bind('mousewheel', function(event, delta, deltaX, deltaY) {
        console.log(delta, deltaX, deltaY);
    });
    
    // using the event helper
    $('#my_elem').mousewheel(function(event, delta, deltaX, deltaY) {
        console.log(delta, deltaX, deltaY);
    });
    
# Limit frequency

Additionally, a timeout can be added as a parameter to limit the number of times per second the event can be triggered. 

    // Add a max frequency of 200 milliseconds (5 times per second)
    $('#my_elem').mousewheel(fn, 200);
    

## License

This plugin is licensed under the MIT License (LICENSE.txt).

Copyright (c) 2011 [Brandon Aaron](http://brandonaaron.net)
