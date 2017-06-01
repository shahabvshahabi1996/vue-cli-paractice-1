<template>
  <div id="box">
    <ul>
        <li v-for= "team in teams" @click = "team.show = !team.show">
            <h3>{{team.name}}&nbsp;{{team.family}}</h3>
            <h5 v-show="team.show">{{team.job}}</h5>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
  data () {
    return {
        teams : [
            {name : 'Shahab' , family : 'Shahabi' , job : 'Web-Designer / Front-end Developer' , show : false},
            {name : 'Arash' , family : 'Dargahi' , job : 'Back-end Developer / Project Manager', show : false},
            {name : 'Siamak' , family : 'Sarmady', job: 'Buissness Manager' , show : false},
            {name : 'Amir' , family : 'Dadgar' , job : 'Android Developer', show : false},
        ]
    }
  },
  methods:{
  }
}
</script>

<style scoped>
  #box{
     width:100%;
     margin : 40px auto;
     padding : 0 20px;
     box-sizing:border-box;
  }
  ul{
    display:flex;
    flex-wrap:wrap;
    list-style-type:none;
    padding:0;
  }
  li{
      flex-grow:1;
      flex-basis:45%;
      text-align:center;
      background-color:#ccc;
      margin:5px;
      border-radius:3px;
      height:100px;
  }
</style>
