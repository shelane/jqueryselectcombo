A 'Select Combo' is setting the values of a select element based on the user's choice of the source select element.  As a jQuery plugin, it will create 'unobtrusive' javascript to bind a change event to the source select element and retrieve JSON results from your server, placing the results in the target select element.  This has been tested with jQuery 1.2.6. on FF 2 & 3, IE7, Safari.  I hope this works with other browsers, but if it doesn't please let me know. (There is an error in IE 6.  I'm currently unsure of what to do with the non helpful MS error of: "Could not set the selected property.  Unspecified error")

This plugin requires [jQuery](http://jquery.com) - a most awesome javascript library for AJAX, AHAH, and all that!

See the [Demo of the selectCombo plugin](http://lasso.pro/selectCombo/)

Rob D from down under has posted a demo using a [large set of data](http://www.msxhost.com/jquery/linked-selects/shelane/)

9/9/2008 - Bypassed select first object for IE - no more IE 6 error

8/29/2008 - 1.2.5 Release - Fixed bug that only called change for children if the hidetarget had been set.

6/24/2008 - 1.2.4 Release - Fixed functionality when selectCombo is used for multiple select objects.  Will now execute the change event for each of the successive targets on change of the parent.

3/1/2007 - 1.2.3 Release - Changed when the hidetarget was called so that targets aren't hidden onchange unless there are no values returned for targets

12/15/2007 - 1.2.2 Release - Fixed issue with target not hiding when there are no options in target

8/30/2007 - 1.2.1 Release - removed console.log line that may cause problems in IE

8/22/2007 - 1.2 Release added option to set target options when the page loads (you may have a default value selected in the primary select that you want to "preload" options in your target)

Clearing options of target before calling getJSON (if primary not same as target) so that if no results are returned target reflects no results of selected primary (if you want there to be something loaded as a place holder for the target, have your server return something like: [{oV: '', oT: '-No Option-'}]

Changed check on hidetarget.  Instead of checking that the primary select has no selected value, will now check that the target has no value.
If hidetarget == true, target will hide onload when no value in target and will hide if no options available on change

5/25/2007 - 1.1 Release added option for indicator display during ajax call, added check that if target ID is the same as the original source, it will override hidetarget setting and not hide target