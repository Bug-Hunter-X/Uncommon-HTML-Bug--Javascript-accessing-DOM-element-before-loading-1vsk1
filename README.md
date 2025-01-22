# Uncommon HTML Bug: Javascript accessing DOM element before loading

This repository demonstrates a subtle bug in HTML where Javascript code attempts to access and manipulate a DOM element before that element has fully loaded into the DOM tree. This is a common issue for beginners, and frequently occurs when Javascript is placed in the `<head>` section of the HTML or if the script runs before the targeted element renders in the DOM.

## Bug Description
The `bug.html` file contains Javascript code that attempts to get an element and modifies it's content. However, this code executes before the element with id `myDiv` is fully loaded into the DOM. As a consequence, the `innerHTML` property cannot be set, leading to a silent failure - no error messages appear, and expected behavior does not occur. 

## Solution
The `bugSolution.html` file demonstrates a solution using the `DOMContentLoaded` event listener. This listener ensures the Javascript code executes only after the entire DOM tree is fully loaded, avoiding the issue of premature access to elements.