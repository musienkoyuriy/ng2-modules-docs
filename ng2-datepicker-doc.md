# Datepicker

The Angular2 Datepicker is a highly configurable modular component that adds date and time picker functionality to your pages. 
You can customize the date and time formats, language, and use selectable date ranges as well as apply CSS styles.

# Table of contents
1. [Importing dependencies](#dependencies)
2. [Usage](#usage)
3. [Examples](#examples)
    1. [Date range picker](#daterange)
    2. [Restrict date range](#restrictrange)
    3. [Single date picker](#singledate)
    4. [Time picker](#singletime)
    5. [Datepicker & Time picker](#datetime)
    6. [Predefined ranges](#predef)
4. [Localization](#localization)
5. [Styling](#styling)
6. [API Reference](#apiref)
    1. [Properties](#properties)
    2. [Events](#events)
    3. [Methods](#methods)


## Importing dependencies <a name="dependencies"></a>
```ng2-bootstrap datepicker``` currently relies on [`Moment.js`](http://momentjs.com/) to format date, so it's necessary to install it.:
```
# install typings globally
npm install -g typings
# init typings if you don't have typings.json yet
typings init
# and install moment.js typings
typings install moment --save
```
Also, please update system.js config to setup mapping:

```javascript
<!-- index.html -->
  System.config({
    packages: {
      app: {
        format: 'register',
        defaultExtension: 'js'
      }
    },
    map: {
      moment: 'node_modules/moment/moment.js'
    }
  });
```
And you should be ready to go! :)
## Usage <a name="usage"></a>
```typescript
import { DatepickerModule } from 'ng2-bootstrap/ng2-bootstrap';
```
## Examples <a name="examples"></a>
### Date Range Picker <a name="daterange"></a>
The date range picker can be attached to a text input or embedded to a web page. It will use the current value of the input to initialize, and update the input if new dates are chosen.

`Code examples:`
#
`Example`
# 
### Pop-up example

`Code examples:`
#
`Example`
# 
### Inline example

`Code examples:`
#
`Example`
# 
#
### Restrict date range <a name="restrictrange"></a>
Restrict the range of selectable dates with the minDate and maxDate options. Set the beginning and end dates as actual dates (?Date=null), as a numeric offset from today ```code```, or as a string of periods and units ```code```. For the last, use 'dd' for days, 'MMMM' for months, or 'yyyy' for years.

`Code examples:`
#
`Example`
# 

### Single date picker <a name="singledate"></a>
The date range picker can be turned into a single datepicker widget with only one calendar. In this example, drop-downs for month and year selection can be found at the top of the calendar to quickly switch between months.

### Pop-up example

`Code examples:`
#
`Example`
# 
### Inline example

`Code examples:`
#
`Example`
# 
### Time picker <a name="singletime"></a>
Standalone ```ng2-bootsrap timepicker``` directive is now deprecated, instead, you can use ```<code>``` from ```ng2-bootstrap datepicker```.

`Code examples:`
#
`Example`
# 
In case you need time picker support along with datepicker, you can add <code> to <file>

### Date & Time picker <a name="datetime"></a>

`Code examples:`
#
`Example`
# 
### Predefined ranges <a name="predef"></a>
Predefined ranges allows to show the option to predefine date ranges that the user can choose from a list.

`Code examples:`
#
`Example`
# 
## Localization <a name="localization"></a>
Datepicker supports calendar language and format (English / Western formatting is the default) localization. The datepicker includes built-in support for languages that read right-to-left, such as Arabic and Hebrew. Apart from in-code localization support datepicker control also supports localization by recognizing different regional options exposed from the browser and also supports validation.

`Code examples:`
#
`Example`
# 
## Styling <a name="styling"></a>
Styling allows to customize the calendar theme, so that calendar theme that will correspond to overall website design. To  designbs-date-picker.css

`Code examples:`
#
`Example`
#  

## API Reference <a name="apiref"></a>
### Properties <a name="properties"></a>
```typescript
ngModel (:Date) - binds to date
datepickerMode (?string='day') - sets datepicker mode, supports: day, month, year
minDate (?Date=null) - oldest selectable date
maxDate (?Date=null) - latest selectable date
dateDisabled (?Array<{date:Date, mode:string}>) - array of disabled dates if mode is day, or years, etc.
customClass (?Array<{date:Date, mode:string, clazz:string}>) - array of custom css classes to be applied to targeted dates
showWeeks (?boolean=true) - if false week numbers will be hidden
startingDay (?number=0) - starting day of the week from 0-6 (0=Sunday, ..., 6=Saturday).
initDate (?Date) - default date to show if ng-model value is not specified
minMode (?string='day') - set lower datepicker mode, supports: day, month, year
maxMode (?string='year') - sets upper datepicker mode, supports: day, month, year
formatDay (?string='dd') - format of day in month
formatMonth (?string='MMMM') - format of month in year
formatMear (?string='yyyy') - format of year in year range
formatDayHeader (?string='EEE') - format of day in week header
formatDayTitle (?string='MMMM yyyy') - format of title when selecting day
formatMonthTitle (?string='yyyy') - format of title when selecting month
yearRange (?number=20) - number of years displayed in year selection
shortcutPropagation (?boolean=false) - if true shortcut`s event propagation will be disabled
onlyCurrentMonth (?boolean=false) - if true only dates from the currently displayed month will be shown
```
### Events <a name="events"></a>
```typescript
```
### Methods <a name="methods"></a>
```typescript
```
<!--

### Usage
```javascript
import { DatepickerModule } from 'ng2-bootstrap/ng2-bootstrap';
// or
import { DatepickerModule } from 'ng2-bootstrap/components/datepicker';
```
### Annotations
```javascript
// component DatePicker
@Component({
  selector: 'datepicker[ngModel], [datepicker][ngModel]'
})
```
# Options, Methods & Events
As the examples demonstrate above ```ng2-bootstrap datepicker``` has many useful options:
```javascript
ngModel (:Date) - binds to date
datepickerMode (?string='day') - sets datepicker mode, supports: day, month, year
minDate (?Date=null) - oldest selectable date
maxDate (?Date=null) - latest selectable date
dateDisabled (?Array<{date:Date, mode:string}>) - array of disabled dates if mode is day, or years, etc.
customClass (?Array<{date:Date, mode:string, clazz:string}>) - array of custom css classes to be applied to targeted dates
showWeeks (?boolean=true) - if false week numbers will be hidden
startingDay (?number=0) - starting day of the week from 0-6 (0=Sunday, ..., 6=Saturday).
initDate (?Date) - default date to show if ng-model value is not specified
minMode (?string='day') - set lower datepicker mode, supports: day, month, year
maxMode (?string='year') - sets upper datepicker mode, supports: day, month, year
formatDay (?string='dd') - format of day in month
formatMonth (?string='MMMM') - format of month in year
formatMear (?string='yyyy') - format of year in year range
formatDayHeader (?string='EEE') - format of day in week header
formatDayTitle (?string='MMMM yyyy') - format of title when selecting day
formatMonthTitle (?string='yyyy') - format of title when selecting month
yearRange (?number=20) - number of years displayed in year selection
shortcutPropagation (?boolean=false) - if true shortcut`s event propagation will be disabled
onlyCurrentMonth (?boolean=false) - if true only dates from the currently displayed month will be shown
```-->
