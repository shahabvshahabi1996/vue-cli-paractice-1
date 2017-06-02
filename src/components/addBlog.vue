<template>
  <div id="app">
    <h2>Add a New Blog Post</h2>
    <form>
        <blog-field></blog-field>
    </form>
  </div>
</template>

<script>

import BlogFields from './blogFields.vue'
export default {
  components : {
   'blog-field' : BlogFields 
  },
  data () {
    return {
    }
  },
  methods:{
    
  }
}
</script>

<style scoped>
h2{
    text-align:center;
}
</style>
