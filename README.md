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
 - [1.2](#1.2) <a name='1.'2></a> **custom_component** : One of the most powerfull features in MeteorKitchen. 
 To add a `custom_component` choose the components in Designer, click `Add new` and select `custom_component` from the list. You can use custom_component in at least 3 different ways.
  - Provide name in `Custom template`. This makes MeteorKitchen look for two files (`Custom template`.html and `Custom template`.fs). Just input the name of the files without extension. Inside those files write normal Meteor template and javascript code.
  - Use the special `TEMPLATE_NAME` magic string in both `HTML code` and `JS code` to make MeteorKitchen automatically use correct name for both the `template` and in `JS code`. Also calls the Template using the Meteor way in the parent HTML. E.g. `{> TEMPLATE_NAME}` gets inserted into the parent HTML with the template code somewhere near it.
```javascript
HTML code
<template name="TEMPLATE_NAME">
  
<button type="submit" id="printPdf" class="printPdf button button-primary">
  <span class="fa fa-print">Print to PDF</span>
</button>

</template>
```
```javascript
JS code

Template.TEMPLATE_NAME.events({
		"click #printPdf": function(e, t) {
		e.preventDefault();

		console.log("Printing...");
	}
});
```
 - Don't use the magic string `TEMPLATE_NAME` and don't wrap your HTML inside `<template>` is what's called the `inline`mode. In `inline`mode the HTML gets inserted into parent HTML "as is".
 
**[⬆ back to top](#table-of-contents)**

# }
