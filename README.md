# Uncommon HTML Bug: Using visibility instead of display for showing hidden elements

This repository demonstrates a subtle yet impactful bug in HTML related to how elements are displayed when their visibility is changed.

## The Bug
The `bug.html` file contains a simple HTML structure with a div initially hidden. A button should show the div upon clicking.  The solution attempts to make it visible using `visibility: visible;` which often seems to work, but has pitfalls.

Incorrectly using `visibility` to show hidden elements can lead to issues where the element remains visually hidden, especially if it was initially hidden using `display: none;`

## The Solution
The `bugSolution.html` file shows the corrected code which uses `display: block;` to properly show the hidden element.  This ensures the element is fully integrated into the page flow.

## Key Differences
* `display: none;` removes the element entirely from the page layout. Changing `display` to `block` or `inline` inserts it back into the layout.
* `visibility: hidden;` hides the element but it still occupies space in the layout.  Changing `visibility` to `visible` just makes it appear without affecting the space it occupies.

This bug highlight the importance of selecting the correct CSS property when controlling element visibility for different layout behaviours.