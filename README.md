# meteor-kitchen-hacks-n-tips for full support {

*meteor-kitchen hacks and snippets*

inspired by [Airbnb JavaScript Style Guide() {](https://github.com/airbnb/javascript)

Please fork this and create pull request to have your hacks-n-tips included ;)

[![kitchen-site](https://img.shields.io/badge/kitchen--site-github-brightgreen.svg)](https://github.com/perak/kitchen-site/)
[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/perak/kitchen-site?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)


## Table of Contents
1. [Display helpers](#helpers)
1. [Template](#template)
1. [Template](#template)


## Helpers
- [1.1](#1.1) <a name='1.1'></a> **Custom HTML output**: When you want to generate custom HTML for a field. Put the helper code somewhere in client area. Either in "Client startup code" in Designer or ```"client_startup_code": "console.log(\"Client startup running \",Meteor.user().profile.name );\n\n",``` in JSON.
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
