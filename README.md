# codeHighlighter
> A jQuery plugin to add HTML markup to various types of computer programming code to make it display and appear beautifully within a HTML document.

## How to use

Simply include the `jquery.codeHighlighter.js` or the `jquery.codeHighlighter.min.js` file and place the following somewhere within the JavaScript code of your web application (make sure **jQuery** is included):

### Minimum Setup

```js
$(function () {
    $.codeHighlighter();
});
```

**Example With Default Options**

```js
$(function () {
    $.codeHighlighter({
        linebreaks: true, // 
        tabSize: 4, //
    });
});
```