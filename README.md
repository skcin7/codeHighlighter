# codeHighlighter
> A jQuery plugin to add HTML markup to various types of computer programming code to make it display and appear beautifully within a HTML document.

## How To Use

Simply include the `jquery.codeHighlighter.js` or the `jquery.codeHighlighter.min.js` file and place the following somewhere within the JavaScript code of your web application (NOTE: make sure **jQuery** is included too, obviously):

### Initialize codeHighlighter In Your Projects

```js
$(function () {
    $.codeHighlighter();
});
```

With this, codeHighlighter will be applied to all nodes within your HTML document's DOM which have the `codeHighlighter` CSS class applied to it.

### Settings/Configuration

You can easily configure codeHighlighter on a per-instance basis, or a per-case basis.

```js
$(function () {
    $.codeHighlighter({
        "highlight": true, // Whether or not the highlighting should take place. Set this to false to disable the code highlighting from being processed
        "linebreaks": true, // Whether linebreaks should be added by default to the final formatted code
        "tabSize": 4, // If the code uses linebreaks, this is the size that each tab should be for each line in the outputted code
    });
});
```

