# Uncommon HTML Bug: Accessing Non-Existent Element

This repository demonstrates a common but often overlooked error in JavaScript when interacting with the HTML DOM: attempting to access a property of an element that doesn't exist.  This usually results in a runtime error because `document.getElementById()` returns `null` if the element isn't found, and trying to access a property of `null` will throw a `TypeError`.

## Bug

The `bug.html` file contains a script that tries to get the `innerHTML` of an element with the ID 'nonExistentId'. Since this element does not exist in the HTML, this results in a JavaScript error. 

## Solution

The `solution.html` file demonstrates the solution. Before accessing any property of the element, always check if `document.getElementById()` returned a valid element (not null).