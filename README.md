# ColorPickerInput
Simple color picker Vue.js component. Based on Bootstrap input type color.

## Just import component and use v-model, example:

``` html
<template>
  <div>
    <div class="col-md-3">
       <ColorPickerInput v-model="color" lebel-name="Test Color"/>
    </div>
 </div>
</template>

<script>
import ColorPickerInput from './ColorPickerInput';

export default {
  name: "TestColorPicker",
  components: {
    ColorPickerInput,
  },
data() {
  return {
    color: '#4D53B3'
   }
  }
}
```

## Props to customize, you can rewrite it by use this properties:

// prop="default" //
  
- label-name="Color" // String;

- label-class="mb-2" // By default got bootstrap class "mb-2" - String;

- style-picker-position="left: 5px" // If you want color picker to be on the right of the input just change it to "right: 5px";

- style-padding-picker="padding-left: 35px;" // If you want color picker to be on the right change it to "padding-right: 35px";

- main-class="form-group" // Main div class

- input-class="form-control" // Input class
