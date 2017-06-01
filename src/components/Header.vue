<template>
  <header>
    <h1>{{title}}</h1>
  </header>
</template>

<script>
export default {
  data () {
    return {
     title : "Vue Farvadin",
    }
  },
  methods:{
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
