<template>
<my-comp 
:abc="fatherText" 
:changeClick="changeClick">
</my-comp>
</template>

<script>
import { ref } from 'vue'
import myComp from './views/myComp.vue'
export default {
  components: { myComp },

  setup() {
    console.log("sss")
    const fatherText = ref("父组件传值")
    function changeClick(val){
      fatherText.value = val;
    }
    return {
      fatherText,
      changeClick
    }
  }
}
</script>