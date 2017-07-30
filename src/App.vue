<template>
  <div id="app">
    <components-a
      msgFromFather="I am a father"
      v-on:child-tell-me-something="lisenToMyBoy"
     ></components-a>
     <p>child tell me {{childWords}}</p>
  </div>
</template>

<script>
import ComponentsA from './components/componentsA'

export default {
  //1.注册 父-子
  components: {ComponentsA},
  data() {
    return{
      childWords:''
    }
  },
  methods: {
    //2.绑定子组件事件 子-父
    lisenToMyBoy(msg){
     // console.log(msg);
     this.childWords=msg
    }
  }
}
</script>

<style>
</style>
