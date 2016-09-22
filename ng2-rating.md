# Rating
Rating component that will take care of visualising a star rating bar

1. [Usage](#usage)
2. [Examples](#examples)
    1. [Static rating](#static)
    2. [Dynamic rating](#dynamic)
    3. [Custom icons](#icons)
3. [API Reference](#api)
    1. [Properties](#properties)
    2. [Events](#events)
    3. [Methods](#methods)
    4. [Annotations](#annotations)
    
## Usage <a name="usage"></a>
```typescript
import { RatingModule } from 'ng2-bootstrap/ng2-bootstrap';
```
## Examples <a name="examples1"></a>
### Static rating <a name="static"></a>
Render a rating widget for display purpose only and prevent any editing ability for the user.
### Dynamic rating <a name="dynamic"></a>
Automatically convert any input to a bootstrap star rating control 
Drag and slide across for changing ratings for better effects on touch input devices.
### Custom icons <a name="icons"></a>
ng2-rating supports any glyphicons instead of stars.
Note: Bootstrap 4 does not include glyphicons anymore, so if you want to continue use this font, you will need to add a link to [glyphicons.css](https://github.com/valor-software/ng2-bootstrap/blob/master/demo/assets/css/glyphicons.css)
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
        <td>max (?number=5)</td>
        <td>number of icons</td>
      </tr>
    </tbody>
    <tbody>
          <tr>
            <td>readonly (?boolean=false)</td>
            <td>if true will not react on any user events</td>
          </tr>
        </tbody>
        <tbody>
              <tr>
                <td>titles (?Array&lt;string&gt;) </td>
                <td>array of icons titles, default: (["one", "two", "three", "four", "five"])</td>
              </tr>
            </tbody>
            <tbody>
        <tbody>
              <tr>
                <td>stateOn (?string='glyphicon-star')</td>
                <td>selected icon class</td>
              </tr>
            </tbody>
            <tbody>
        <tbody>
              <tr>
                <td>stateOff (?string='glyphicon-star-empty')</td>
                <td>unselected icon class</td>
              </tr>
            </tbody>
            <tbody>
        <tbody>
              <tr>
                <td>ratingStates (?{stateOn:string, stateOff:string}[])</td>
                <td>array of custom icons classes</td>
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
        <td>onHover</td>
        <td>fired when icon selected, $event:number equals to selected rating</td>
      </tr>
      <tr>
        <td>onLeave</td>
        <td>fired when icon selected, $event:number equals to previous rating value</td>
      </tr>
    </tbody>
  </table>
</div>

### Methods <a name="methods"></a>

<div class="table-responsive">
  <table class="table table-bordered table-striped">
    <thead>
      <tr>
        <th style="width: 150px;">Method Type</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>update</td>
        <td>update the rating by setting a value. The method accepts a rating value as a parameter.</td>
      </tr>
      <tr>
        <td>refresh</td>
        <td>use this method to dynamically refresh the rating options. This method returns the rating input element as an object and can thus be chained with other methods.</td>
      </tr>
      <tr>
        <td>reset</td>
        <td>resets the rating to the initial value.</td>
      </tr>
      <tr>
        <td>clear</td>
        <td>clears the rating</td>
      </tr>
    </tbody>
      <tr>
        <td>destroy</td>
        <td>destroys the rating</td>
      </tr>
      <tr>
        <td>create</td>
        <td>creates the rating after destroying any existing rating instance.</td>
      </tr>
  </table>
</div>

### Annotations <a name="annotations"></a>

```typescript
// class Rating implements on Init
@Component({
  selector: 'rating[ngModel]'
})
export class RatingComponent implements ControlValueAccessor, OnInit {
  @Input() private max:number;
  @Input() private stateOn:string;
  @Input() private stateOff:string;
  @Input() private readonly:boolean;
  @Input() private titles:Array<string>;
  @Input() private ratingStates:{stateOn:string, stateOff:string}[];

  @Output() private onHover:EventEmitter<number> = new EventEmitter(false);
  @Output() private onLeave:EventEmitter<number> = new EventEmitter(false);
}
```