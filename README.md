# Uncommon HTML Error: Handling Null or Undefined Objects

This repository demonstrates two subtle errors that can occur in HTML/JavaScript when dealing with potentially null or undefined objects.

## Error 1: Accessing Properties of a Null Object
The first error showcases the issue of trying to access properties of an element that doesn't exist in the DOM.  `document.getElementById` returns `null` if the element isn't found, leading to a runtime error if you subsequently try to access its properties (innerHTML, textContent etc.).

## Error 2: Accessing Element Before it's loaded
The second error highlights a common mistake in which Javascript tries to access the content of an HTML element before that element has finished loading completely, this leads to an error because the element's properties might not be ready yet.

## Solution
The solution involves adding checks to ensure that the element exists and that it has finished loading before accessing its properties.  Always check for null or undefined values before using them.

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Inspect the browser's console; you'll see the error messages.
4. Open `bugSolution.html` and observe how the solution avoids the errors.
