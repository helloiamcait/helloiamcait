# Customizing a form dropdown

While building an app with the MEAN stack and Bootstrap, I wanted to customize a dropdown in a form. The dropdown looked like this:

![Screenshot 2023-10-10 at 2 00 51 PM](https://github.com/helloiamcait/helloiamcait/assets/85128509/d2897bc4-8f99-4994-852f-eb3d5e1b2274)

There were two attributes that I wanted to display in the dropdown automatically:

  1.  [Floating label](#display-a-floating-label)
  2.  [Default null option](#display-a-default-null-option)

## Display a floating label

Add the following to display a floating label in the dropdown:
  -  `form-floating` 
  -  `aria-label="Floating label select example"`
  -  `<label for="floatingSelect">PLACEHOLDER_LABEL</label>`

### Example
#### Code
```html
<div class="mb-3 form-floating">
    <select class="form-select" id="level" formControlName="level" aria-label="Floating label select example">
      <option id="level-internship" value="internship">Internship</option>
      <option id="level-entry" value="entry">Entry</option>
      <option id="level-associate" value="associate">Associate</option>
      <option id="level-mid-senior" value="mid-senior">Mid-Senior</option>
      <option id="level-director" value="director">Director</option>
      <option id="level-executive" value="executive">Executive</option>
    </select>
    <label for="floatingSelect">Position Level</label>
</div>
```
#### Output
![Screenshot 2023-10-10 at 1 56 13 PM](https://github.com/helloiamcait/helloiamcait/assets/85128509/6fc20084-2232-47dc-9cc0-5953a99515f3)

## Display a default null option

Add the following to display a default null value in the dropdown:
  -  `<option [ngValue]="null" disabled>PLACEHOLDER_NULL_VALUE</option>`

### Example
#### Code
```html
<div class="mb-3 form-floating">
    <select class="form-select" id="level" formControlName="level" aria-label="Floating label select example">
      <option [ngValue]="null" disabled>Choose...</option>
      <option id="level-internship" value="internship">Internship</option>
      <option id="level-entry" value="entry">Entry</option>
      <option id="level-associate" value="associate">Associate</option>
      <option id="level-mid-senior" value="mid-senior">Mid-Senior</option>
      <option id="level-director" value="director">Director</option>
      <option id="level-executive" value="executive">Executive</option>
    </select>
    <label for="floatingSelect">Position Level</label>
</div>
```
#### Output
![Screenshot 2023-10-10 at 1 56 56 PM](https://github.com/helloiamcait/helloiamcait/assets/85128509/7b8716a7-dfcf-43cb-a956-cd6f0fdff417)
