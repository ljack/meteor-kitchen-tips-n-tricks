# meteor-kitchen-hacks for full support {

*meteor-kitchen hacks and snippets*

inspired by [Airbnb JavaScript Style Guide() {](https://github.com/airbnb/javascript)

[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/perak/kitchen-site?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)


## Table of Contents
1. [Display helpers](#helpers)
1. [Template](#template)
1. [Template](#template)


## Helpers
- [1.1](#1.1) <a name='1.1'></a> **Custom HTML output**: When you want to generate custom HTML for a field.
```javascript
Template.registerHelper("displayPhoto",  function (url) {
  let html = `<img src="${url}" />`;
  return Spacebars.SafeString(html);
} );
```
**[⬆ back to top](#table-of-contents)**

## Template
 - [x.x](#x.x) <a name='x.'x></a> ** Add stuff here ** : That helps make meteorkitchen more fun ;) 
 
**[⬆ back to top](#table-of-contents)**

# }
