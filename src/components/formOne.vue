<template>
  <div id="app">
   <!-- <app-header></app-header>
    <app-content></app-content>
    <app-footer></app-footer> -->
    <form-helper>
      <div slot="form-header">
        <h3>This is a form header For Login</h3>
        <p>This is the Login Form</p>
      </div>
      <div slot="form-fields">
        <input type="text" placeholder="name" requierd/>
        <br><br>
        <input type="password" placeholder="password" requierd/>
      </div>
      <div slot="form-controls">
      <br>
        <button>Submit</button>
      </div>
    </form-helper>
  </div>
</template>

<script>
import Formhelper from './formhelper.vue'

export default {
  components : {
    'form-helper' : Formhelper,
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
