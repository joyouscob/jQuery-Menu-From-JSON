# JSON to Menu
jQuery Plugin for create multilevel menus from a JSON String
## Features
* Create a Multilevel Menu as Unordered List
* Create a multilevel select (Indented)
# 1. How to use
## 1.1. Creating a Indented Select (input select AKA combobox)
#### HTML Code
```html
<div class="col-md-4">
  <div id="container_id"></div>
</div>
```
#### Javascript Code
```javascript
var str_json = '[ { "value": "#", "text": "Products", "children": [ { "value": "#", "text": "Books", "children": [ { "value": "#", "text": "Jquery" }, { "value": "#", "text": "Codeigniter" }, { "value": "#", "text": "Wordpress" } ] }, { "value": "#", "text": "Software" } ] }, { "value": "#", "text": "Sites", "children": [ { "value": "//davicotico.com", "text": "My Blog" }, { "value": "#", "text": "GitHub" } ] } ]';

$(document).ready(function(){
    $('#container_id').jsontomenu({
        data: str_json, 
        type: 'select', 
        title: '-Select an Option-',
        active: '//davicotico.com'
    });
});

```
## 1.2. Indented Select (Populate the Select)
#### HTML Code
```html
<div class="col-md-4">
  <select id="select_id" class="form-control"></select>
</div>
```
#### Javascript Code
```javascript
$(document).ready(function(){
    $('#select_id').jsontomenu({
        data: str_json, 
        type: 'fill_select', 
        title: '-Select an Option-',
        active: '//davicotico.com'
    });
});

```
## 1.3. Creating an Unordered List
You need a JSON string with this data:
```
[
{
"href": "",
"text": "",
"icon": "",
"target": "",
"alt": "",
"children": 
 [
 ...
 ]
}
]
```
#### HTML Code
```html
<div class="col-md-4">
  <div id="container_id"></div>
</div>
```
#### Javascript Code
```javascript
$(document).ready(function(){
    $('#container_id').jsontomenu({
        data: str_json, 
        type: 'list', 
        title: 'Main Menu',
        active: '//davicotico.com'
    });
});
```
