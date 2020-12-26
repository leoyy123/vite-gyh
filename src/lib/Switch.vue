<template>
    <button @click="toggle" class="button" :class="{checked:value}"><span></span></button>
</template>
<script lang="ts">
import {ref} from 'vue';
export default {
  props:{
    value:Boolean
  },
  setup(props,context) {
    const checked= ref(false);
    const toggle=()=>{
      // checked.value=!checked.value;
      context.emit('input',!props.value)
    }
    return {checked,toggle};
  }
};
</script>
<style lang="scss" scoped>
$h: 22px;
  $h2: $h - 4px;
.button {
  height: $h;
  width: $h*2;
  border: none;
  background: gray;
  border-radius: $h/2;
  position: relative;
  outline: none;
}
span {
  position: absolute;
  top: 2px;
  left: 2px;
  height: $h2;
  width: $h2;
  background: white;
  border-radius: $h2/2;
  transition: left 0.2s;
}
.button.checked{
  background: blue;
}
.button.checked>span{
  left: 22px;
}
</style>