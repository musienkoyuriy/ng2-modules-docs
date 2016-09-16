# Dropdowns

A dropdown menu is a toggleable menu that allows the user to choose one value from a predefined list. They’re made interactive with the included dropdown directives.

Base specifications: [bootstrap 3](http://getbootstrap.com/javascript/#dropdowns) or [bootstrap 4](http://v4-alpha.getbootstrap.com/components/dropdowns/)


1. [Examples](#examples1)
    1. 
    1. [Expand direction](#direction)
    2. [Menu alignment](#alignment)
    3. [Custom Classes & Styling options](#styling)
    4. [Headers](#content)  
    5. [Divider](#examples4)
    6. [Disabled menu items](#examples2)
    7. [Button state]
    8. [Trigger actions]    
    9. [Dropdown Accessibility]
2. [Usage](#usage)
3. [API Reference](#api)
4. [Dropdown properties](#properties)
5. [Events](#events)
6. [Toggle properties]()
7. [Methods](#methods)
 
## Examples <a name="examples1"></a>
### Expand direction <a name="direction"></a>
Dropdown menu can expand both upwards and downwards, change the <div> element with class="dropdown" to "dropup". Default behaviour is `dropdown`
#
`code1`
#
`Example`

### Menu aligment
By default, a dropdown menu is automatically positioned 100% from the top and along the left side of its parent. Add .dropdown-menu-right to a .dropdown-menu to right align the dropdown menu.
#
`code1`
#
`Example`

### Custom Classes & Styling options
You may use simple bootstrap classes, customized CSS or third party add-ons to create beautiful looking dropdown menus
#
`code1`
#
`Example`

### Headers
The .dropdown-header class is used to add headers inside the dropdown menu:
#
`code1`
#
`Example`

### Dividers
The .divider class is used to separate links inside the dropdown menu with a thin horizontal border:
#
`code1`
#
`Example`

### Disabled menu items
To disable an item in the dropdown menu, use the `.disabled` class:
#
`code1`
#
`Example`

### Button state
To disable the button itself, add `disabled` class to the button:
#
`code1`
#
`Example`

### Trigger actions
#
`code1`
#
`Example`

### Dropdown Accessibility
Dropdowns have native support for keyboard navigation. Just add role="menu" to your dropdown-menu
#
`code1`
#
`Example`

## API Reference <a name="api"></a>
### Dropdown properties <a name="properties"></a>
```typescript
isOpen (?boolean=false) - if true dropdown will be opened
autoClose (?string='nonInput') - behaviour vary:
nonInput - (default) automatically closes the dropdown when any of its elements is clicked — as long as the clicked element is not an input or a textarea.
always - automatically closes the dropdown when any of its elements is clicked
outsideClick - closes the dropdown automatically only when the user clicks any element outside the dropdown
disabled - disables the auto close. You can then control the open/close status of the dropdown manually, by using is-open. Please notice that the dropdown will still close if the toggle is clicked, the esc key is pressed or another dropdown is open
keyboardNav (?boolean=false) - if true will enable navigation of dropdown list elements with the arrow keys
appendToBody (not yet tested) (?boolean=false) - if true dropdownMenu content will be appended to the body. This is useful when the dropdown button is inside a div with overflow: hidden, and the menu would otherwise be hidden
```
### Events <a name="events"></a>
```typescript
onToggle - fired when dropdown toggles, $event:boolean equals dropdown isOpen state
```
### Methods <a name="methods"></a>
```
.dropdown("toggle")	- Toggles the dropdown
```
