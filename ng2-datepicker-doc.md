# Datepicker

The Angular2 Datepicker is a highly configurable modular component that adds date and time picker functionality to your pages. You can customize the date and time formats, language, and use selectable date ranges as well as apply CSS styles.

# Usage
```ng2-datepicker``` currently relies on [`Moment.js`](http://momentjs.com/) to format date.
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
#
The default date picker functionality is that it's tied to a standard form input field. Focus on the input (click, or use the tab key) to open an interactive calendar in a small overlay. Choose a date, click elsewhere on the page (blur the input), or hit the Esc key to close. If a date is chosen, feedback is shown as the input's value.

# Single Date Picker
The date range picker can be turned into a single date picker widget with only one calendar. In this example, drop-downs to select a month and year have also been enabled at the top of the calendar to quickly jump to different months.
### Example
#
# Date Range Picker
The date range picker can be attached to a text input or embedded to a web page. It will use the current value of the input to initialize, and update the input if new dates are chosen.
### Pop-up example
### Embedded example

#
# Restrict date range
Restrict the range of selectable dates with the minDate and maxDate options. Set the beginning and end dates as actual dates (?Date=null), as a numeric offset from today ```code```, or as a string of periods and units ```code```. For the last, use 'dd' for days, 'MMMM' for months, or 'yyyy' for years.
### Example
#
# Time Picker
Standalone timepicker directive is now deprecated, instead, you can use <code> from ```ng2-datepicker```.
### Example

In case you need date picker with time picker support, you can add <code> to <file>

### Date picker with time picker support example

#
# Predefined Ranges
Predefined ranges allows to show the option to predefine date ranges that the user can choose from a list.
### Example
#
# Localization
Localize the date picker calendar language and format (English / Western formatting is the default). The date picker includes built-in support for languages that read right-to-left, such as Arabic and Hebrew.  Datepicker control supports localization by recognizing different regional options exposed from the browser and also supports validation.
### Example
#
# CSS Styling
```ng2-datepicker``` supports CSS Styling, so you can customize the calendar theme, so that calendar theme that will correspond to your overall. To  designbs-date-picker.css
### Example
Restrict the range of selectable dates with the minDate and maxDate options. Set the 
#
# Options, Methods & Events
As the examples demonstrate above ng2-datepicker has many useful options:
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
```