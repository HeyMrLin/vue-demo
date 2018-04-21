<template>
  <div class="first">
    <router-link to="/">我是第一个模版</router-link>
    <button @click="changeMsg">click</button>
    <child-component :message='message'></child-component>
  </div>
</template>
import childComponent from ''
<script>
  import childComponent from './childTemplate/childComponent'

  export default {
    name: "first-component",
    data(){
      return {
        message:"爸爸给的!",
      }
    },
    methods:{
      changeMsg(){
        this.message="爸爸不给了!";
      }
    },
    components: {
      childComponent
    }
  }
</script>

<style scoped>
  .first {
    color: #42b983;
  }
</style>
