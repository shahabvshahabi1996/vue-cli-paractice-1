<template>
   <div>
        <div id="form-fields">
         <div v-if="!submited">
            <label id="label">Blog Title</label>
            <input type="text" id="title_name" v-model="title" placeholder="Choose a Title For Your Blog" required/>
            <br>
            <label id="label">Blog Content</label>
            <textarea name="" id="textarea" cols="30" v-model="content" rows="10" placeholder="Type What Ever You Want..."></textarea>
            <div id="authores">
                <label for="">Choose the Author</label>
                <select name="" id="" v-model="author">
                    <option v-for="writer in writers" :value="writer">{{writer}}</option>
                </select>              
            </div>
            <div id="checkboxes">
            <p>Choose a Categoery For Your Post</p>
                <div class="checkbox">
                    <label>Sience</label>
                    <input type="checkbox" value="Sience" v-model="Categoery"/>
                </div>
                <div class="checkbox">
                    <label>Technology</label>
                    <input type="checkbox" value="Technology" v-model="Categoery"/>
                </div>
                <div class="checkbox">
                    <label>Information</label>
                    <input type="checkbox" value="Information" v-model="Categoery"/>
                </div>
                <div class="checkbox">
                    <label>Quetes</label>
                    <input type="checkbox" value="Quetes" v-model="Categoery"/>
                </div>
            </div>
            <button id="post" v-on:click.prevent="HandleSubmit">Add Blog</button>
        </div>
         </div>
            
       <!-- <div id="form-controls">
            <button @click="">Post</button>
        </div>-->
        <h2 v-if="submited" style="text-align:center">Thank You for Adding Your Blog</h2>
        <div v-if="submited">
            <h3 style="text-align:center;">Preview Blog</h3>
        <div id="preview">
            <h4>Blog Title</h4>
            <p>{{title}}</p>
            <h4>Blog Content</h4>
            <p>{{content}}</p>
            <p>The Author : {{author}}</p>
            <h4>Post Category</h4>
            <ul>
                <li v-for="category in Categoery">{{category}}</li>
            </ul>
        </div>
        </div>
    </div>
</template>

<script>
export default {
  data () {
    return {
     title:" ",
     content:" ",
     Categoery : [],
     author : " ",
     writers : ['Shahab','Arash','Amir'],
     post : {
        blogTitle : "",
        blogContent : "",
        blogAuthor : "",
        blogCat : [],
     },
     submited : false,
    }
  },
  methods:{
    HandleSubmit : function(){
        this.post.blogTitle = this.title;
        this.post.blogContent = this.content;
        this.post.blogAuthor = this.author;
        this.post.blogCat = this.Categoery;
        console.log(this.title);
        console.log(this.content);
        console.log(this.author);
        console.log(this.Categoery);
        this.$http.post('https://jsonplaceholder.typicode.com/posts',{
          title : this.title,
          body : this.content,
          userId : 1
      }).then(function(data){
          //console.log(data);
          this.submited = true;
      });
    },    
  }
}
</script>

<style scoped>
#preview{
    padding:10px;
    border : 4px dashed #ccc;
    width:40%;
    margin: 40px auto;
    height:auto;
}
#title_name{
    width:200px;
    display:block;
    margin: 5px auto;
    text-align:left;
    width:100%;
    border-color:#ccc;
    border-style:solid;
    border-width:2px;
    border-radius:3px;
    box-shadow:none;
    outline:none;
    height:30px;
}
#textarea{
    display:block;
    margin: 5px auto;
    text-align:left;
    width : 100%;
    border-color:#ccc;
    border-style:solid;
    border-width:2px;
    border-radius:3px;
    box-shadow:none;
    outline:none;
}
#form-fields{
    margin : 0 auto;
    padding:10px;
    width : 40%;
}
#label{
    text-align:left;
}
.checkbox{
    display:inline-block;
    margin:10px;
}
#post{
    background-color:#fff;
    color:#252525;
    border: 1px solid #252525;
    border-radius:3px;
}
</style>
