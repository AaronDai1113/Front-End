<template>
  <div id="nav">
    12345---{{name}}-{{id}}----{{n}} <br>
    <button @click="active()">click</button>
  </div>
</template>

<script>
import { computed, reactive, toRef, toRefs } from 'vue'
export default {
  setup(){
    const state=reactive({
      name:'abc',
      id:1,
      n:computed(()=>state.id-1)
    })
    const active = ()=>{
      console.log(123);
      return state.id+=1;
    }
    return {
      ...toRefs(state),
      active
    }
  }
}
</script>
<style>

</style>
