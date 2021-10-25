# HTML-Internationalization
### HTML Internationalization for WebExtensions
The code is modular so it can be used verbatim without any need for any change. It can be used for Options pages, Browser Action pop-ups, Page Action pop-ups, Sidebar or any other HTML document.

The Internationalization is done by adding a `data-i18n` attribute to the elements.

If `data-i18n` does not have a `|` then the localised message will be appended to the node as TEXT.  
If `data-i18n` has a `id|attribute` then the localised message will be set to the node attribute.

**Notes** 
- The Internationalization is added as TEXT as I believe locales should not contain HTML
- HTML Internationalization is meant for static values and dynamic values should be set by JavaScript

### Examples (from -> to)

```html
<p data-i18n="someText"></p>
<p data-i18n="someText">someText Message</p>`

<p data-i18n="someText"><img src="" alt=""> </p>
<p data-i18n="someText"><img src="" alt=""> someText Message</p>`

<p><span data-i18n="someText"></span></p>
<p><span data-i18n="someText">someText Message</span></p>`
```

Passing to a `value` or any other attribute:  
Just add the attribute name after `|`

```html
<input type="button" data-i18n="someText|value" value="">
<input type="button" data-i18n="someText|value" value="someText Message">

<a href="https://github.com/" data-i18n="someText|title" target="_blank"><span data-i18n="otherText"></span></a>
<a href="https://github.com/" data-i18n="someText|title" title="someText" target="_blank"><span data-i18n="otherText">otherText</span></a>
```

### Further Development
So far, I have not come across a situation that couldn't be handled (or made to be handled) by the code. Let me know of such instances and I will update the code accordingly.
