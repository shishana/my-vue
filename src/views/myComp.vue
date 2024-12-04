<template>
  <button @click="changeClick('子组件修改')">change</button>
  <div>{{abc}}</div>
</template>

<script>
export default {

  props: {
    abc: {
      type: String,
      defult: null
    },
    changeClick: {
      type:Function
    }
  },

  setup() {
    return {
    }
  }
}
</script>