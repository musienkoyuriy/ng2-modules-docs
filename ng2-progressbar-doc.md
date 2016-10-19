#Progressbar
Progress bar is a component used to show the progress of a given process.

# Table of contents
1. [Usage](#usage)
2. [Examples](#examples)
    1. [Static](#static)
    2. [Dynamic](#dynamic)
    3. [Stacked](#stacked)
4. [Styling](#styling)
5. [API Reference](#apiref)
    1. [Properties](#properties)
    2. [Annotations](#annotations)

#Usage <a name="usage"></a>
Importing progressbar module:
```typescript
import { ProgressbarModule } from 'ng2-bootstrap/ng2-bootstrap';
```
#Examples <a name="examples"></a>
##Static <a name="static"></a>
Default progress bar.

`Code examples:`

`Example`

Default progress bar with percentage.

`Code examples:`

`Example`

##Dynamic <a name="dynamic"></a>
Example of dynamic progressbar with right to left stripes animation 


`Code examples:`

`Example`


##Stacked <a name="stacked"></a>
Progessbar component allows merging multiple bars into one to stack them.


`Code examples:`

`Example`

#Styling <a name="styling"></a>
All progress indicators can be themed. There are four supported contextual classes: success, info, warning, danger

`Example`

## API Reference <a name="apiref"></a>

### Properties <a name="properties"></a>
<div class="table-responsive">
  <table class="table table-bordered table-striped">
    <thead>
      <tr>
        <th style="width: 150px;">Property</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>value (*number) </td>
        <td>current value of progress bar</td>
      </tr>
    </tbody>
     <tbody>
          <tr>
            <td>type (*string)</td>
            <td>provide one of the four supported contextual classes: success,info, warning, danger</td>
          </tr>
        </tbody>
     <tbody>
          <tr>
            <td>max (?number=100)</td>
            <td>maximum total value of progress element</td>
          </tr>
        </tbody>
     <tbody>
          <tr>
            <td>animate (?boolean=true) </td>
            <td>if true changing value of progress bar will be animated (note: not supported by Bootstrap 4)</td>
          </tr>
        </tbody>

  </table>
</div>

