<template>
  <div>
    <div class="child">{{msg}}{{message}}</div>
    <button @click="changeMsgs">click</button>
  </div>
</template>

<script>
  export default {
    name: "child-component",
    data() {
      return {
        msg: "我是子模版"
      }
    },
    watch:{
      msg:function (val,oldVal) {

      }
    },
    methods:{
      changeMsgs(){
        this.msg="我还是一个子模版!";
      }
    },
    props:[
      'message'
    ]
  }
</script>

<style scoped>

</style>
