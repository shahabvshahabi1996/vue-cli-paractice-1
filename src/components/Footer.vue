<template>
  <footer>
    <p>{{ copyright }}</p>
  </footer>
</template>

<script>
export default {
  data () {
    return {
        copyright : "This site made by love and Me ... <3 :)"
    }
  },
  methods:{
  }
}
</script>

<style scoped>
    footer{
        background-color:#222;
        padding:6px;
        bottom:0;
        position:relative;
        text-align:center;
    }
    p{
        color:lightgreen;
    }
</style>
