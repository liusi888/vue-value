<template>
  <div class="hello">
      <h1>{{msg}}</h1>
      <button v-on:click="onClickMe">Click!</button>
  </div>
</template>

<script>
export default {
  //1.接收 父-子
  props:['msgFromFather'],
  data() {
    return {
      msg:'hello from component A'
    }
  },
  methods: {
    onClickMe() {
         //1.打印
        //console.log(this.msgFromFather);
        //2.发送给父级
        this.$emit('child-tell-me-something',this.msg);
     }
  }

}
</script>


<style scoped>

</style>
