# HTML-Internationalization
HTML Internationalization for WebExtension


The code is modular so it can be used verbatim without any need for any change.

Example of Usage:

`<p data-i18n="someText"></p>` -->  
`<p data-i18n="someText">someText Message</p>`

`<p data-i18n="someText"><img src="" alt=""> </p>` -->  
`<p data-i18n="someText"><img src="" alt=""> someText Message</p>`

`<p><span data-i18n="someText"></span></p>` -->  
`<p><span data-i18n="someText">someText Message</span></p>`

Passing to a `value` or any other attribute: 
Just add the attribute name after `|`

`<input type="button" data-i18n="someText|value" value="">` -->  
`<input type="button" data-i18n="someText|value" value="someText Message">`
