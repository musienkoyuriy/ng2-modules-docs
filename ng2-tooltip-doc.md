---
layout: docs
title: Tooltips
group: components
---

Inspired by the excellent Tipsy jQuery plugin written by Jason Frame. Tooltips are an updated version, which don’t rely on images, use CSS3 for animations, and much more.

Base specifications: [bootstrap 3](http://getbootstrap.com/javascript/#tooltips) or [bootstrap 4](http://v4-alpha.getbootstrap.com/components/tooltips/)

## Contents

1. [Overview](#overview)
2. [Examples](#examples1)
    1.1 [Dynamic Tooltip Pop-up & Text](#examples2)
    1.2 [Custom Class, TemplateRef and HTML in tooltips](#examples3)
    1.3 [Custom Triggers & conditions](#examples4)
3. [Another paragraph](#paragraph2)

## Overview <a name="overview"></a>

Things to know when using the tooltip plugin:

- Tooltips with zero-length titles are never displayed.
- Specify `container: 'body'` to avoid rendering problems in more complex components (like our input groups, button groups, etc).
- Triggering tooltips on hidden elements will not work.
- Tooltips for `.disabled` or `disabled` elements must be triggered on a wrapper element.
- When triggered from hyperlinks that span multiple lines, tooltips will be centered. Use `white-space: nowrap;` on your `<a>`s to avoid this behavior.

Got all that? Great, let's see how they work with some examples.


## Examples <a name="examples1"></a>

### Dynamic Tooltip Text <a name="examples2"></a>
```code1```
```Example```
### Dynamic Tooltip Popup Text
```code2```
```Example2```

### Custom Class, TemplateRef and HTML in tooltips <a name="examples3"></a>
Tooltips can contain any arbitrary HTML, Angular bindings and even directives! Simply enclose desired content in a <template> element.

*HTML*
```code1```
I can even contain HTML. ```Check me out!```

*TemplateRef*
```code2```
Or use a TemplateRef. ```Check me out!```

*Custom Class*
```code3```
I can have a custom class. ```Check me out!```

### Сustom triggers & conditions <a name="examples4"></a>
*Custom triggers*
```code1```
```Example```
*Conditions*
```code2```
```Example2```


## Usage
```typescript
import { TooltipModule } from 'ng2-bootstrap/ng2-bootstrap';
// or
import { TooltipModule } from 'ng2-bootstrap/components/tooltip';
```

## Annotations
```typescript
// class Tooltip implements OnInit
@Directive({ selector: '[tooltip]' })
export class TooltipDirective {
  @Input('tooltip') private content:string;
  @Input('tooltipHtml') public htmlContent:string | TemplateRef<any>;
  @Input('tooltipPlacement') private placement:string = 'top';
  @Input('tooltipIsOpen') private isOpen:boolean;
  @Input('tooltipEnable') private enable:boolean;
  @Input('tooltipAppendToBody') private appendToBody:boolean;
  @Input('tooltipClass') public popupClass:string;
  @Input('tooltipContext') public tooltipContext:any;
}
```

## Tooltip properties
```typescript
  - `tooltip` (`string`) - text of tooltip
  - `tooltipHtml` (`string|TempalteRef`) - tooltip custom html content, defined as string or template reference
  - `tooltipPlacement` (`?string='top'`) - tooltip positioning instruction, supported positions: 'top', 'bottom', 'left', 'right'
  - `tooltipAnimation` (`?boolean=true`) - if `false` fade tooltip animation will be disabled
  - `tooltipPopupDelay` (*not implemented*) (`?numer=0`) - time in milliseconds before tooltip occurs
  - `tooltipTrigger` (*not implemented*) (`?Array<string>`) - array of event names which triggers tooltip opening
  - `tooltipEnable` (`?boolean=true`) - if `false` tooltip is disabled and will not be shown
  - `tooltipAppendToBody` (*not implemented*) (`?boolean=false`) - if `true` tooltip will be appended to body
  - `tooltipClass` (`?string`) - custom tooltip class applied to the tooltip container
  - `tooltipIsOpen` (`?boolean=false`) - if `true` tooltip is currently visible
  - `tooltipContext` (`any`) - if a template is used for the content, then this property can be used to specify a context for that template. The template variable exposed is called 'model'.
```
### Markup
```
<div class="form-group">
  <label>Dynamic Tooltip Text</label>
  <input type="text" [(ngModel)]="dynamicTooltipText" class="form-control">
</div>
<div class="form-group">
  <label>Dynamic Tooltip Popup Text</label>
  <input type="text" [(ngModel)]="dynamicTooltip" class="form-control">
</div>
<p>
  Pellentesque <a href="#" [tooltip]="dynamicTooltip">{{dynamicTooltipText}}</a>,
  sit amet venenatis urna cursus eget nunc scelerisque viverra mauris, in
  aliquam. Tincidunt lobortis feugiat vivamus at
  <a href="#" tooltipPlacement="left" tooltip="On the Left!">left</a> eget
  arcu dictum varius duis at consectetur lorem. Vitae elementum curabitur
  <a href="#" tooltipPlacement="right" tooltip="On the Right!">right</a>
  nunc sed velit dignissim sodales ut eu sem integer vitae. Turpis egestas
  <a href="#" tooltipPlacement="bottom" tooltip="On the Bottom!">bottom</a>
  pharetra convallis posuere morbi leo urna,
  <a href="#" [tooltipAnimation]="false" tooltip="I don't fade. :-(">fading</a>
  at elementum eu, facilisis sed odio morbi quis commodo odio. In cursus
  <a href="#" tooltipPopupDelay='1000' tooltip='appears with delay'>delayed</a> turpis massa tincidunt dui ut.
  nunc sed velit dignissim sodales ut eu sem integer vitae. Turpis egestas
</p>
 
<p>
  I can even contain HTML. <a href="#" [tooltipHtml]="htmlTooltip">Check me out!</a>
</p>
 
<template #toolTipTemplate let-model="model">
  <h4>Tool tip custom content defined inside a template</h4>
  <h5>With context binding: {{model.text}}</h5>
</template>
 
<p>
  Or use a TemplateRef. <a href="#" [tooltipHtml]="toolTipTemplate" [tooltipContext]="tooltipModel">Check me out!</a>
<p>
 
<p>
  I can have a custom class. <a href="#" tooltip="I can have a custom class applied to me!" tooltipClass="customClass">Check me out!</a>
</p>
 
<form role="form">
  <div class="form-group">
    <label>Or use custom triggers, like focus: </label>
    <input type="text" name="clickMe" value="Click me!" tooltip="See? Now click away..."  tooltipTrigger="focus" tooltipPlacement="right" class="form-control" />
  </div>
 
  <div class="form-group" ngClass="{'has-error' : !inputModel}">
    <label>Disable tooltips conditionally:</label>
    <input type="text" name="inputModel" [(ngModel)]="inputModel" class="form-control"
           placeholder="Hover over this for a tooltip until this is filled"
           tooltip="Enter something in this input field to disable this tooltip"
           tooltipPlacement="top"
           tooltipTrigger="mouseenter"
           [tooltipEnable]="!inputModel || inputModel.length==0" />
  </div>
</form>
```
### TypeScript
```typescript
import { ChangeDetectionStrategy, Component } from '@angular/core';
 
// webpack html imports
let template = require('./tooltip-demo.html');
 
@Component({
  selector: 'tooltip-demo',
  template: template,
  changeDetection: ChangeDetectionStrategy.OnPush
})
export class TooltipDemoComponent {
  public dynamicTooltip:string = 'Hello, World!';
  public dynamicTooltipText:string = 'dynamic';
  public htmlTooltip:string = 'I\'ve been made <b>bold</b>!';
  public tooltipModel:any = {text: 'foo', index: 1};
}
```
### Options

Options can be passed via data attributes or JavaScript. For data attributes, append the option name to `data-`, as in `data-animation=""`.

<div class="table-responsive">
  <table class="table table-bordered table-striped">
    <thead>
      <tr>
        <th style="width: 100px;">Name</th>
        <th style="width: 100px;">Type</th>
        <th style="width: 50px;">Default</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>animation</td>
        <td>boolean</td>
        <td>true</td>
        <td>Apply a CSS fade transition to the tooltip</td>
      </tr>
      <tr>
        <td>container</td>
        <td>string | false</td>
        <td>false</td>
        <td>
          <p>Appends the tooltip to a specific element. Example: <code>container: 'body'</code>. This option is particularly useful in that it allows you to position the tooltip in the flow of the document near the triggering element - which will prevent the tooltip from floating away from the triggering element during a window resize.</p>
       </td>
      </tr>
      <tr>
        <td>delay</td>
        <td>number | object</td>
        <td>0</td>
        <td>
         <p>Delay showing and hiding the tooltip (ms) - does not apply to manual trigger type</p>
         <p>If a number is supplied, delay is applied to both hide/show</p>
         <p>Object structure is: <code>delay: { "show": 500, "hide": 100 }</code></p>
        </td>
      </tr>
      <tr>
        <td>html</td>
        <td>boolean</td>
        <td>false</td>
        <td>Insert HTML into the tooltip. If false, jQuery's <code>text</code> method will be used to insert content into the DOM. Use text if you're worried about XSS attacks.</td>
      </tr>
      <tr>
        <td>placement</td>
        <td>string | function</td>
        <td>'top'</td>
        <td>
          <p>How to position the tooltip - top | bottom | left | right | auto.<br>When "auto" is specified, it will dynamically reorient the tooltip. For example, if placement is "auto left", the tooltip will display to the left when possible, otherwise it will display right.</p>
          <p>When a function is used to determine the placement, it is called with the tooltip DOM node as its first argument and the triggering element DOM node as its second. The <code>this</code> context is set to the tooltip instance.</p>
        </td>
      </tr>
      <tr>
        <td>selector</td>
        <td>string</td>
        <td>false</td>
        <td>If a selector is provided, popover objects will be delegated to the specified targets. In practice, this is used to enable dynamic HTML content to have popovers added. See <a href="https://github.com/twbs/bootstrap/issues/4215">this</a> and <a href="http://jsbin.com/zopod/1/edit">an informative example</a>.</td>
      </tr>
      <tr>
        <td>template</td>
        <td>string</td>
        <td><code>'&lt;div class="tooltip" role="tooltip"&gt;&lt;div class="tooltip-arrow"&gt;&lt;/div&gt;&lt;div class="tooltip-inner"&gt;&lt;/div&gt;&lt;/div&gt;'</code></td>
        <td>
          <p>Base HTML to use when creating the tooltip.</p>
          <p>The tooltip's <code>title</code> will be injected into the <code>.tooltip-inner</code>.</p>
          <p><code>.tooltip-arrow</code> will become the tooltip's arrow.</p>
          <p>The outermost wrapper element should have the <code>.tooltip</code> class.</p>
        </td>
      </tr>
      <tr>
        <td>title</td>
        <td>string | element | function</td>
        <td>''</td>
        <td>
          <p>Default title value if <code>title</code> attribute isn't present.</p>
          <p>If a function is given, it will be called with its <code>this</code> reference set to the element that the tooltip is attached to.</p>
        </td>
      </tr>
      <tr>
        <td>trigger</td>
        <td>string</td>
        <td>'hover focus'</td>
        <td>How tooltip is triggered - click | hover | focus | manual. You may pass multiple triggers; separate them with a space. `manual` cannot be combined with any other trigger.</td>
      </tr>
      <tr>
        <td>constraints</td>
        <td>Array</td>
        <td>[]</td>
        <td>An array of constraints - passed through to Tether. For more information refer to Tether's <a href="http://github.hubspot.com/tether/#constraints">constraint docs</a>.</td>
      </tr>
      <tr>
        <td>offset</td>
        <td>string</td>
        <td>'0 0'</td>
        <td>Offset of the popover relative to its target. For more information refer to Tether's <a href="http://github.hubspot.com/tether/#constraints">offset docs</a>.</td>
      </tr>
    </tbody>
  </table>
</div>

 <div class="callout">
 <h2>Data attributes for individual tooltips</h2>
 <p>Options for individual tooltips can alternatively be specified through the use of data attributes, as explained above.</p>
 </div>




### Methods

#### `$().tooltip(options)`

Attaches a tooltip handler to an element collection.

#### `.tooltip('show')`

Reveals an element's tooltip. **Returns to the caller before the tooltip has actually been shown** (i.e. before the `shown.bs.tooltip` event occurs). This is considered a "manual" triggering of the tooltip. Tooltips with zero-length titles are never displayed.

{% highlight js %}$('#element').tooltip('show'){% endhighlight %}

#### `.tooltip('hide')`

Hides an element's tooltip. **Returns to the caller before the tooltip has actually been hidden** (i.e. before the `hidden.bs.tooltip` event occurs). This is considered a "manual" triggering of the tooltip.

{% highlight js %}$('#element').tooltip('hide'){% endhighlight %}

#### `.tooltip('toggle')`

Toggles an element's tooltip. **Returns to the caller before the tooltip has actually been shown or hidden** (i.e. before the `shown.bs.tooltip` or `hidden.bs.tooltip` event occurs). This is considered a "manual" triggering of the tooltip.

{% highlight js %}$('#element').tooltip('toggle'){% endhighlight %}

#### `.tooltip('dispose')`

Hides and destroys an element's tooltip. Tooltips that use delegation (which are created using [the `selector` option](#options)) cannot be individually destroyed on descendant trigger elements.

{% highlight js %}$('#element').tooltip('dispose'){% endhighlight %}

### Events

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
        <td>show.bs.tooltip</td>
        <td>This event fires immediately when the <code>show</code> instance method is called.</td>
      </tr>
      <tr>
        <td>shown.bs.tooltip</td>
        <td>This event is fired when the tooltip has been made visible to the user (will wait for CSS transitions to complete).</td>
      </tr>
      <tr>
        <td>hide.bs.tooltip</td>
        <td>This event is fired immediately when the <code>hide</code> instance method has been called.</td>
      </tr>
      <tr>
        <td>hidden.bs.tooltip</td>
        <td>This event is fired when the tooltip has finished being hidden from the user (will wait for CSS transitions to complete).</td>
      </tr>
    </tbody>
  </table>
</div>
