# Dropdowns

A dropdown menu is a toggleable menu that allows the user to choose one value from a predefined list. They’re made interactive with the included dropdown directives.

Base specifications: [bootstrap 3](http://getbootstrap.com/javascript/#dropdowns) or [bootstrap 4](http://v4-alpha.getbootstrap.com/components/dropdowns/)


1. [Usage](#usage)
2. [Examples](#examples)
    1. [Expand direction](#direction)
    2. [Menu alignment](#alignment)
    3. [Headers](#headers)  
    4. [Divider](#divider)
    5. [Disabled menu items](#disable)
    6. [Button state](#btnstate)
    7. [Trigger actions](#trigger) 
    8. [Dropdown Accessibility](#accessibility)
3. [Styling](#styling)
4. [API Reference](#api)
    1. [Properties](#properties)
    2. [Events](#events)
    3. [Methods](#methods)
    4. [Annotations](#annotations)
 
## Usage <a name="usage"></a>
```typescript
import { DropdownModule } from 'ng2-bootstrap/ng2-bootstrap';
```
## Examples <a name="examples"></a>
### Expand direction <a name="direction"></a>
Dropdown menu can expand both upwards and downwards, change the element with class="dropdown" to "dropup". Default behaviour is `dropdown`

`Code examples:`
#
`Example`
# 
### Menu aligment <a name="alignment"></a>
By default, a dropdown menu is automatically positioned 100% from the top and along the left side of its parent. Add `.dropdown-menu-right` to a `.dropdown-menu` to right-align the dropdown menu.

`Code examples:`
#
`Example`
# 
### Headers <a name="direction"></a>
The `.dropdown-header` class is used to add headers inside the dropdown menu:

`Code examples:`
#
`Example`
# 
### Dividers <a name="direction"></a>
The `.divider` class is used to separate links inside the dropdown menu with a thin horizontal border:

`Code examples:`
#
`Example`
# 
### Disable menu items < a name="direction"></a>
To disable an item in the dropdown menu, use the `.disabled` class:

`Code examples:`
#
`Example`
# 
### Button state <a name="direction"></a>
To disable the button itself, add `disabled` class to the button:

`Code examples:`
#
`Example`
# 
### Trigger actions <a name="direction"></a>
Set custom actions to trigger dropdown action.

`Code examples:`
#
`Example`
# 
### Dropdown Accessibility <a name="direction"></a>
Dropdowns have native support for keyboard navigation. Just add role="menu" to your dropdown-menu
#
`code1`
#
`Example`
## Styling <a name="styling"></a>
Datepicker uses bootstrap classes, customized CSS or third party add-ons to create beautiful looking dropdown menus

`Code examples:`
#
`Example`
# 
## API Reference <a name="api"></a>
### Properties <a name="properties"></a>

<div class="table-responsive">
  <table class="table table-bordered table-striped">
    <thead>
      <tr>
        <th style="width: 150px;">Properties</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>isOpen (?boolean=false)</td>
        <td>if true, dropdown will be opened</td>
      </tr>
    </tbody>
    <tbody>
          <tr>
            <td>autoClose (?string='nonInput')</td>
            <td>behaviour vary, see lower entries for options &darr; </td>
          </tr>
        </tbody>
        <tbody>
              <tr>
                <td>nonInput</td>
                <td>(default) automatically closes the dropdown when any of its elements is clicked — as long as the clicked element is not an input or a text area.</td>
              </tr>
            </tbody>
            <tbody>
        <tbody>
              <tr>
                <td>always</td>
                <td>automatically closes the dropdown when any of its elements is clicked</td>
              </tr>
            </tbody>
            <tbody>
        <tbody>
              <tr>
                <td>outsideClick</td>
                <td>closes the dropdown automatically only when the user clicks any element outside the dropdown</td>
              </tr>
            </tbody>
            <tbody>
        <tbody>
              <tr>
                <td>disabled</td>
                <td>disables the auto close. You can then control the open/close status of the dropdown manually, by using is-open. Please notice that the dropdown will still close if the toggle is clicked, the esc key is pressed or another dropdown is open</td>
              </tr>
            </tbody>
            <tbody>
        <tbody>
              <tr>
                <td>keyboardNav (?boolean=false)</td>
                <td>if true, will enable navigation of dropdown list elements with the arrow keys</td>
              </tr>
            </tbody>
        <tbody>
              <tr>
                <td>appendToBody (not yet tested) (?boolean=false)</td>
                <td>if true, dropdown menu content will be appended to the body. This is useful when the dropdown button is inside a div with overflow: hidden, and the menu would otherwise be hidden</td>
              </tr>
            </tbody>
            <tbody>
  </table>
</div>

### Events <a name="events"></a>
<div class="table-responsive">
  <table class="table table-bordered table-striped">
    <thead>
      <tr>
        <th style="width: 150px;">Event Type</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>onToggle</td>
        <td>Fired when dropdown toggles, $event:boolean equals dropdown isOpen state</td>
      </tr>
    </tbody>
  </table>
</div>

### Methods <a name="methods"></a>
<div class="table-responsive">
  <table class="table table-bordered table-striped">
    <thead>
      <tr>
        <th style="width: 150px;">Method</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>.dropdown("toggle")</td>
        <td>Toggles the dropdown. That simple :)</td>
      </tr>
    </tbody>
  </table>
</div>

### Annotations <a name="annotations"></a>
```typescript
// directive Dropdown
@Directive({
  selector: '[dropdown]',
  exportAs: 'bs-dropdown'
})
export class Dropdown implements OnInit, OnDestroy {
  @HostBinding('class.open')
  @Input() public get isOpen():boolean {}
  @Input() public autoClose:string;
  @Input() public keyboardNav:boolean;
// enum string: ['nonInput', always', 'outsideClick', 'disabled']
  @Input() public appendToBody:boolean;
  @Output() public onToggle:EventEmitter<boolean>;
}

// directive DropdownToggle
@Directive({ 
  selector: '[dropdownToggle]',
  exportAs: 'bs-dropdown-toggle'
})
export class DropdownToggle implements OnInit {
  @HostBinding('class.disabled')
  @Input() public isDisabled:boolean = false;

  @HostBinding('class.dropdown-toggle')
  @Input() public addToggleClass:boolean = false;

  @HostBinding('attr.aria-expanded')
  public get isOpen() {}
  @HostListener('click', ['$event'])
  public toggleDropdown(event:MouseEvent) {}
}
````

