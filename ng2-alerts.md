# Alerts

Provides contextual feedback messages to create alert messages like success, warning, info and error to show important and critical information to the user.

1. [Usage](#usage)
2. [Examples](#examples)
    1. [Types](#types)
    2. [Content](#content)
    3. [Dismissible alerts](#)
3. [API Reference](#api)
    1. [Properties](#properties)
    2. [Events](#events)
    3. [Methods](#methods)
    
## Usage
```typescript
import { AlertModule } from 'ng2-bootstrap/ng2-bootstrap';
```
## Examples
Wrap any text and an optional dismiss button in .alert and one of the four contextual classes (e.g., .alert-success) for basic alert messages.

> Alerts don't have default classes, only base and modifier classes. A default gray alert doesn't make too much sense, so you're required to specify a type via contextual class. Choose from success, info, warning, or danger.

## Types
There are four types of alerts: 
### `alert-success`
```html
<div class="alert alert-success" role="alert">...</div>
```
`example`
### `alert-info`
```html
<div class="alert alert-info" role="alert">...</div>
```
`example`
### `alert-warning`
```html
<div class="alert alert-warning" role="alert">...</div>
```
`example`
### `alert-danger`
```html
<div class="alert alert-danger" role="alert">...</div>
```
`example`  
###
## Content
Alerts can contain various content, starting from links, to HTML and TemplateRef.

Use the .alert-link utility class to quickly provide matching colored links within any alert.
```html
<a href="#" class="alert-link">...</a>
```
## Dismissible alerts
Alerts have `dismiss` option. Build on any alert by adding an optional `.alert-dismissible` and add additional close button.
```html
<div class="alert alert-warning alert-dismissible" role="alert">
  <button type="button" class="close" data-dismiss="alert" aria-label="Close"><span aria-hidden="true">&times;</span></button>
  Hello there, young man. Could you please close me?
</div>
```

## API Reference
### Properties
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
        <td>type (?:string='warning') </td>
        <td>provide one of the four supported contextual classes: success,info, warning, danger</td>
      </tr>
    </tbody>
 <tbody>
      <tr>
        <td>dismissible (?:boolean=false) </td>
        <td>determines if an inline close button is displayed</td>
      </tr>
    </tbody>
     <tbody>
      <tr>
        <td>dismissOnTimeout (?number=0)</td>
        <td>number of milliseconds, if specified sets a timeout duration, after which the alert will be closed</td>
      </tr>
    </tbody>
  </table>
</div>

### Events
<div class="table-responsive">
  <table class="table table-bordered table-striped">
    <thead>
      <tr>
        <th style="width: 150px;">Events</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>close</td>
        <td>fired when <b>alert</b> closed with inline button or by timeout, $event is an instance of Alert component</td>
      </tr>
    </tbody>
    <tbody>
      <tr>
        <td>closed</td>
        <td>fired when <b>alert</b> when the alert message has been closed</td>
      </tr>
    </tbody>
   </table>
</div>

### Methods

<div class="table-responsive">
  <table class="table table-bordered table-striped">
    <thead>
      <tr>
        <th style="width: 150px;">Methods</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>.alert("close")</td>
        <td>Closes the alert message</td>
      </tr>
    </tbody>
   </table>
</div>