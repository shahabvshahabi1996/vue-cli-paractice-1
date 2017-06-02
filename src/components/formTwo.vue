<template>
  <div id="app">
   <!-- <app-header></app-header>
    <app-content></app-content>
    <app-footer></app-footer> -->
    <form-helper>
      <div slot="form-header">
        <h3>This is a form header For Comment</h3>
        <p>This is a Commenting Form</p>
      </div>
      <div slot="form-fields">
        <input type="text" placeholder="name" requierd/>
        <br><br>
        <textarea name="" id="FormTwo-TextArea" placeholder="Comment Your Massage Here.." cols="30" rows="10"></textarea>
      </div>
      <div slot="form-controls">
      <br>
        <button>Send</button>
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
