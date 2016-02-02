# meteor-kitchen-hacks
meteor-kitchen hacks and snippets 

## Table of Contents
1. [Display helpers for any custom HTML for fields](#helpers)
2. das
3. 


## Helpers
- [1.1](#1.1)
```javascript
Template.registerHelper("displayPhoto",  function (url) {
  let html = `<img src="${url}" />`;
  return Spacebars.SafeString(html);
} );
```
