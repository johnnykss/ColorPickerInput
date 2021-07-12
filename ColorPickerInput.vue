<template>
  <div :class="mainClass">
    <label :class="labelClass" v-text="labelName"></label>
    <div class="color-picker">
      <input v-model="localColor" type="text"
             placeholder="#000000"
             :class="inputClass"
             :style="stylePaddingPicker"
      >
      <input type="color"
             class="color-picker__color"
             v-model="localColor"
             :style="[
                 {background: (localColor.length > 0 && localColor.length === 7) ? localColor : '#000000'},
                 stylePickerPosition
                 ]"
      >
    </div>
  </div>
</template>

<script>
export default {
  name: "ColorPickerInput",
  props: {
    value: {
      type: String,
      default: '#000000'
    },
    labelName: {
      type: String,
      default: 'Color'
    },
    labelClass: {
      type: String,
      default: 'mb-2'
    },
    stylePickerPosition: {
      type: String,
      default: 'left: 5px;'
    },
    stylePaddingPicker: {
      type: String,
      default: 'padding-left: 35px;'
    },
    mainClass: {
      type: String,
      default: 'form-group'
    },
    inputClass: {
      type: String,
      default: 'form-control'
    },
  },
  computed: {
    localColor: {
      get() {
        return this.value
      },
      set(val) {
        this.$emit('change', val)
        this.$emit('input', val)
      }
    }
  }
}
</script>

<style lang="scss">

.color-picker {
  position: relative;

  input:not([type=color]) {
    text-transform: uppercase;
  }

  &__color {
    display: block;
    position: absolute;
    width: 26px;
    height: 26px;
    padding: 0;
    border-color: transparent;
    border-radius: 50%;
    top: calc(50% - 13px);

    &:focus {
      outline: none;
    }

    &::-webkit-color-swatch {
      border: none;
    }
  }
}

</style>
