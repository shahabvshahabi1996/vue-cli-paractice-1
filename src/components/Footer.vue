<template>
  <footer>
    <p>{{ copyright }} by {{title}}</p>
  </footer>
</template>

<script>
import { bus } from '../main'
export default {
  data () {
    return {
        title : "Farvardin",
        copyright : "This site made by love and Me ... <3 :)"
    }
  },
  methods:{
  },
  created(){
    bus.$on('TitleChanged', (data) => {
      this.title = data;
    })
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
