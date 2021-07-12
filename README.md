# ColorPickerInput
Simple color picker Vue.js component. Based on Bootstrap input type color.

## Just import component and use v-model, example:

``` html
<template>
  <div>
    <div class="col-md-3">
       <ColorPickerInput class="form-group" v-model="color" lebel-name="Test Color"/>
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

| Prop                          | Type       | Default             | Description                                      |
|-------------------------------|------------|---------------------|--------------------------------------------------|
| label-name                    | String     | Color               | Label Name under the input                       |
| placeholder                   | String     | #000000             | Input placeholder                                |
| label-class                   | String     | mb-2                | Label class                                      |
| style-picker-position         | Object     | {left: '5px'}       | Picker absolute position in input                |
| style-padding-picker          | String     | padding-left: 35px; | Input padding in input to split text from picker |
| input-class                   | String     | form-control        | Input class                                      |

