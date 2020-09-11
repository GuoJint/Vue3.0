<template>
  <div>
    Vue3.0
    <h1>x: {{position}}</h1>
  </div>
</template>

<script>
import { reactive } from 'vue'
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  setup(){
    //reactive 把一个数据模型加工为一个响应式的数据模型
    const position = reactive({})

    window.addEventListener('mousemovw',(e)=>{
      position.x = e.pageX
      position.y = e.pageY
    })

    return ({position})
  }
}
</script>
