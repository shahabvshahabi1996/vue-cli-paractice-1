<template>
  <div id="app">
    <app-header></app-header>
    <app-content></app-content>
    <app-footer></app-footer> 
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Content from './components/Content.vue'
export default {
  components : {
    'app-header' : Header,
    'app-footer' : Footer,
    'app-content' : Content
  },
  data () {
    return {
    }
  },
  methods:{
  }
}
</script>

<style>
  body{
    color:#252525;
  }
</style>
