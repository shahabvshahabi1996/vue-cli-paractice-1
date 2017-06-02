<template>
  <header>
    <h1 @click="ChangeTitle">{{title}}</h1>
  </header>
</template>

<script>
import { bus } from '../main'
export default {
  data () {
    return {
     title : "Vue Farvadin",
    }
  },
  methods:{
    ChangeTitle : function(){
      bus.$emit('TitleChanged' , 'Team');
    },
  }
}
</script>

<style scoped>
    header{
        padding:15px;
        background-color:lightgreen;
        text-align:center;
    }
    h1{
        color:#252525;
    }
</style>
