# Tabs

Add dynamic tab menu with dropdown functionality to navigate through panes of local content. **Nested tabs are not supported.**

Base specifications: [bootstrap 3](http://getbootstrap.com/javascript/#tabs) or [bootstrap 4](http://v4-alpha.getbootstrap.com/components/navs/)


1. [Usage](#usage)
2. [Examples](#examples)
    1. [Multiple tabs](#multiple)
    2. [Dynamic tabs]
    3. [Tabs with dropdown menu](#dropdowns)
    4. [Pills](#pills)  
    5. [Vertical Pills](#v_pills_)
    6. [Pills with dropdown menu](#droppills)
    7. [Toggleable Tabs & Pills ](#toggletab)
    8. [Tab accessibility](#tabaccessibility) (?) Accessibility Plugin (?)
3. [Styling](#styling)
4. [API Reference](#api)
    1. [Annotations](#annotations)
    2. [Tabset properties](#tabset)
    3. [Tab properties](#tab)
    4. [Events](#events)
    5. [Tab heading](#heading)

## Usage <a name="usage"></a>

Importing tab module:
```typescript
import { TabsModule } from 'ng2-bootstrap/ng2-bootstrap';
```
Tabs are created with `<tabset>`:
```html
<tabset>
  <tab heading='Tab 1'>Tab 1 content</tab>
  <tab>
    <template tab-heading>Tab 2</template>
    Tab 2 content
  </tab>
</tabset>
```

## Examples <a name="examples"></a>
### Multiple tabs
Create a simple tab-based navigation bar.

`Code examples:`
#
`Example`
#  
### Dynamic tabs
#### HTML tab heading
Tab menu headings can contain HTML.

`Code examples:`
#
`Example`
#           
#### Closable tab
Create a closable tab.

`Code examples:`
#
`Example`
#   
### Tabs with dropdown menu
Tab-based navigation bar can hold dropdown menus.
`Code examples:`
#
`Example`
#  

### Pills
Display the menu with Pills instead of Tabs.
`Code examples:`
#
`Example`
# 
### Vertical pills
Vertical placement of pills-based menu.
`Code examples:`
#
`Example`
# 
### Pills with dropdown Menu
Display the menu with Pills instead of tabs, that can hold dropdown menus.
`Code examples:`
#
`Example`
# 
### Toggleable Tabs & Pills
To make the tabs toggleable, add the data-toggle="tab" attribute to each link and and data-toggle="pill" for pills respectively.
`Code examples:`
#
`Example`
# 
 
### Tab accessibility
Tabs support keyboard-only navigation, to enable accessibility, add
`Code examples:`
#
`Example`
# 
## Styling

## API Reference
### Annotations
```typescript
// component Tabset
@Component({
  selector: 'tabset'
})
export class TabsetComponent implements OnInit {
  @Input() public vertical:boolean;
  @Input() public justified:boolean;
  @Input() public type:string;
}

// directive Tab
@Directive({ selector: 'tab, [tab]' })
export class TabDirective implements OnInit, OnDestroy, DoCheck {
  @Input() public heading:string;
  @Input() public disabled:boolean;
  @Input() public removable:boolean;

  /** tab active state toogle */
  @HostBinding('class.active')
  @Input() public get active() {}

  @Output() public select:EventEmitter<Tab> = new EventEmitter(false);
  @Output() public deselect:EventEmitter<Tab> = new EventEmitter(false);
  @Output() public removed:EventEmitter<Tab> = new EventEmitter(false);
}

// directive TabHeading
@Directive({selector: '[tab-heading]'})
export class TabHeadingDirective {}
```

### Tabset properties

<div class="table-responsive">
  <table class="table table-bordered table-striped">
    <thead>
      <tr>
        <th style="width: 150px;">Tabset property</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>vertical (?boolean=false)</td>
        <td>if true tabs will be placed vertically</td>
      </tr>
    </tbody>
     <tbody>
          <tr>
            <td>justified (?boolean=false)</td>
            <td>if true tabs fill the container and have a consistent width</td>
          </tr>
        </tbody>
     <tbody>
          <tr>
            <td>type (?string='tabs')</td>
            <td>navigation context class: 'tabs' or 'pills'</td>
          </tr>
        </tbody>        
  </table>
</div>

### Tab properties
<div class="table-responsive">
  <table class="table table-bordered table-striped">
    <thead>
      <tr>
        <th style="width: 150px;">Tab property</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>heading (string)</td>
        <td>tab header text</td>
      </tr>
    </tbody>
     <tbody>
          <tr>
            <td>active (?boolean=false)</td>
            <td> if tab is active equals true, or set true to activate tab</td>
          </tr>
        </tbody>
     <tbody>
          <tr>
            <td>disabled (?boolean=false)</td>
            <td>if true tab can not be activated</td>
          </tr>
        </tbody>        
     <tbody>
          <tr>
            <td>removable (?boolean=false) </td>
            <td>if true tab can be removed, additional button will appear</td>
          </tr>
        </tbody>  
  </table>
</div>

### Tab events

<div class="table-responsive">
  <table class="table table-bordered table-striped">
    <thead>
      <tr>
        <th style="width: 150px;">Tab events</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>select</td>
        <td>fired when tab became active, $event:Tab equals to selected instance of Tab component</td>
      </tr>
    </tbody>
     <tbody>
          <tr>
            <td>deselect</td>
            <td>fired when tab became inactive, $event:Tab equals to deselected instance of Tab component</td>
          </tr>
        </tbody>
     <tbody>
          <tr>
            <td>removed</td>
            <td>fired before tab will be removed</td>
          </tr>
        </tbody>        
  </table>
</div>