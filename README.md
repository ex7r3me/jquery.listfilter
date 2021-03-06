Listfilter
----------

Listfilter is a jQuery plugin for filtering HTML lists. Check out the [demo](http://astutech.github.io/jquery.listfilter/) and try the [tests](http://astutech.github.io/jquery.listfilter/tests/)

How do I use it?
================

An example:

    $('ul#mylist').listfilter({
        'filter': $('input#mylistfilter'),
        'clearlink': $('a#clearmylistfilter')
    });

Creating a filtered list
========================

To create a filtered list, you need two things as a minimum:

* An HTML list to filter
* A text input to enter the text to filter by into

Assuming that the list you want to filter has an ID of mylist and the filter is an input with an id of myfilter, the following would set up a listfilter:

    $('ul#mylist').listfilter({
        'filter': $('input#myfilter')
    });

This is the bare minimum you need to create a listfilter, but there are other settings.

Settings
========

The following settings can be passed through on initialisation:

* **filter** - The input element you wish users to enter text into in order to filter
* **clearlink** (Optional) - A clickable element, such as a button or link. When clicked, this will clear the text in the filter and reset the list to its default state
* **alternate** (Optional) - Sometimes you may want to differentiate between adjacent elements in a list by alternating the CSS to improve readability. If alternate is set to true, a class will be applied to every second element in the list. This will remain consistent even when filtered.
* **alternateclass** (Optional) - If alternate is set to true, the default class to be applied to every other element is 'alternate'. If you don't want to use this, you can pass through an alternative class to apply to alternate elements
* **callback** (Optional) - A function that calls after filtering done

Refresh
=======

If you wish to programmatically add or remove list items, and are using the alternate option, you'll need to call this to ensure the alternate class is applied correctly afterwards. You can call it as follows:

    $('ul#mylist').listfilter("refresh");

Tests
=====

Listfilter comes with its own QUnit test suite. You can find this in the tests folder 

License
=======

GPLv2
