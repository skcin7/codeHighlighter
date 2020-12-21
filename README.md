# codeHighlighter
> A jQuery plugin to add HTML markup to various types of computer programming code to make it display and appear beautifully within a HTML document.
>
> **Homepage:** [https://skcin7.github.io/codeHighlighter/](https://skcin7.github.io/codeHighlighter/)

## How To Use

Simply include the `jquery.codeHighlighter.js` (or the `jquery.codeHighlighter.min.js`) file and place the following somewhere within the JavaScript code of your web application (NOTE: make sure **jQuery** is included too, obviously):

## Initialize codeHighlighter

```js
$(function () {
    $.codeHighlighter();
});
```

codeHighlighter will now be applied to all nodes in your HTML document which have the `codeHighlighter` CSS class applied to it. For example:

```html
<div class="codeHighlighter" data-language="json">{"some_json_key": "some_json_value", "etc": "etc"}</div>
```

In the above example, the raw/unformatted JSON in the div node will now be formatted in to beautiful looking JSON!

## Settings/Configuration

codeHighlighter is configurable, which is easy to do. Each configuration setting may be applied on a per-instance basis or a per-case basis.

```js
$(function () {
    $.codeHighlighter({
        "highlight": true,    // Whether or not to process the highlighting. Set to false to disable the highlighting from taking place.
        "linebreaks": true,   // Whether or not linebreaks should be added to the final outputted code
        "tabSize": 4,         // The size each tab should be in the outputted code (only applicable if the outputted code uses linebreaks)
    });
});
```

You may also change the configuration for each individual element within the HTML document by using the `data-` attributes of the individual element. Here's some examples:

The following will NOT process the highlighting, because of the `data-highlight=false` data attribute:

```html
<div class="codeHighlighter" data-language="json" data-highlight="false">{"some_json_key": "some_json_value", "etc": "etc"}</div>
```

The following changes the linebreaks and tab size to be used for the final processed code to be displayed in the HTML document:

```html
<div class="codeHighlighter" data-language="json" data-highlight="true" data-linebreaks="false" data-tab-size="2">{"some_json_key": "some_json_value", "etc": "etc"}</div>
```

## CSS

codeHighlighter relies on some CSS code in order for the highlighting to be properly displayed, for adding things like color. Make sure you include the CSS. If your project uses a CSS pre-processor such as SCSS (which I use), you may add the SCSS to your project, which is located in the `/src/scss` directory within this repository. You may also just add the raw CSS code too. If you're in need of something like codeHighlighter, I imagine that this is second-nature and hopefully very obvious to you.

You may extend or alter the CSS (if you want) by adding additional CSS code that will overwrite the default CSS.

```css
.codeHighlighter {
    font-family: "Courier New", Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
    font-size: 12px;
    line-height: 1.5;
}
```

If you do add any custom CSS code, make sure you add it AFTER codeHighlighter's CSS code (or use `!important` in each CSS property) , or else the codeHighlighter CSS code will take priority (in which case your custom CSS would not take effect).

## Contributing

Please see [CONTRIBUTE.md](CONTRIBUTE.md) for information regarding contributing.

## Demo

Please see the [demo page](https://skcin7.github.io/codeHighlighter/demo/) for an example of how codeHighlighter works, and some of the things you can do with it.