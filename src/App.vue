<template>
  <div id="app">
   <!-- <app-header></app-header>
    <app-content></app-content>
    <app-footer></app-footer> -->
   <!-- <button v-on:click="TabtoFormOne">Form 1</button>
    <button v-on:click="TabtoFormTwo">Form 2</button> -->
  <!--  <keep-alive>
      <component v-bind:is="component"></component>
    </keep-alive>-->
   <!-- <add-blog></add-blog>-->
   <show-blog></show-blog>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Content from './components/Content.vue'
import Formhelper from './components/formhelper.vue'
import FormOne from './components/formOne.vue'
import FormTwo from './components/formTwo.vue'
import AddBlog from './components/addBlog.vue'
import ShowBlogs from './/components/showBlogs.vue'

export default {
  components : {
    'app-header' : Header,
    'app-footer' : Footer,
    'app-content' : Content,
    'form-helper' : Formhelper,
    'form-one' : FormOne,
    'form-two' : FormTwo,
    'add-blog' : AddBlog,
    'show-blog' : ShowBlogs,
  },
  data () {
    return {
      title:"I am a Slot Title",
      component : 'form-one',
    }
  },
  methods:{
    TabtoFormOne:function(){
      this.component = 'form-one';
    },
    TabtoFormTwo:function(){
      this.component = 'form-two';
    },
  }
}
</script>

<style>
  body{
    color:#252525;
  }
  *{ 
    border-box:box-sizing;
  }
</style>
