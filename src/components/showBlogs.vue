<template>
  <div id="show-blog">
    <div id="titlebar">
        <h1>All Blog Articales</h1>
    </div>  
    <div v-for="blog in blogs" class="single-blog">
        <h3>{{blog.id}}.{{blog[i]}}{{blog.title}}</h3>
        <p>{{blog.body}}</p>
    </div>
  </div>    
</template>

<script>


export default {
  data () {
    return {
        blogs : [],
    }
  },
  methods:{ 

   
  },
  created(){
    this.$http.get('https://jsonplaceholder.typicode.com/posts').then(function(data){
        this.blogs = data.body       
        console.log(this.blogs);
    });
  },
}
</script>

<style>
  .single-blog{
      background-color:#eee;
      padding:15px;
      margin:10px auto;
      width:50%;
  }
  #titlebar{
      width:50%;
      margin:10px auto;
  }
</style>
