<template>
  <div id="nav">

  </div>
</template>

<script>
import { reactive } from 'vue'
export default {
  setup(){
    const state=reactive({
      name:'abc',
      id:1
    })
    return state;
  }
}
</script>
<style>

</style>
