<template>
 <div>
   <Switch :value="checked" @input="checked=$event"></Switch>
 </div>
</template>
<script lang="ts">
import Switch from '../lib/Switch.vue';
import {ref} from 'vue';
export default {
    components:{
      Switch
    },
    setup() {
      const checked = ref(false);
      return {checked}
    }
}
</script>
<style lang="scss" scoped>

</style>