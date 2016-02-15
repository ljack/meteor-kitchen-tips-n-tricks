# meteor-kitchen-tips-tricks for full support {

*meteor-kitchen tips-n-tricks and snippets*

inspired by [Airbnb JavaScript Style Guide() {](https://github.com/airbnb/javascript)

Please fork this and create pull request to have your hacks-n-tips included. Or create an issue, if you can't find the tip you're looking for.

[![kitchen-site](https://img.shields.io/badge/kitchen--site-github-brightgreen.svg)](https://github.com/perak/kitchen-site/)
[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/perak/kitchen-site?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)


## Table of Contents
1. [Display helpers](#helpers)
1. [custom_component](#custom_component)
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

## custom_component
 - [1.2](#1.2) <a name='1.'2></a> ** Custom component ** : One of the most powerfull features in MeteorKitchen. 
 To add a `custom_component` choose the components in Designer, click `Add new` and select `custom_component` from the list. You can use custom_component in at least 3 different ways.
  1. Provide name in `Custom template`. This makes MeteorKitchen look for two files (`Custom template`.html and `Custom template`.fs). Just input the name of the files without extension.


**[⬆ back to top](#table-of-contents)**

# }
