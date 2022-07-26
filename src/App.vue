<template>
  <div class="black-bg" v-if="모달창열렸냐">
    <div class="white-bg">
      <h4>상세페이지임</h4>
      <p @click="모달창열렸냐=false">내용임</p>
    </div>
  </div> 

  <div class="menu">
    <a v-for="메뉴목록 in 메뉴들" :key="메뉴목록">{{메뉴목록}}</a>
  </div>
  <div class="container">
    <div v-for="i in data" :key="i" @click="모달창열렸냐=true" class="content">
      <h4 >{{i.title}}</h4>
      <p>{{i.price}}</p>
      <p>{{i.content}}</p>
      <img :src="i.image" alt="img"/>
    </div>
  </div>
</template>

<script>
import data from "./assets/data.js";
export default {
  name: 'App',
  data(){
    return{
      data : data,
      모달창열렸냐 : false,
      신고수: [0,0,0,0],
      메뉴들 : ["Home","Shop","About"],
      동네들:["","역삼동","천호동","마포구"],
      이미지:["", './images/room0.jpg', './images/room1.jpg', './images/room2.jpg'],
    }
  },
  methods :{
    신고수초기화하기(){
      for(var i=0; i<4; i++){
        this.
        신고수[i]=0;
    }
    }
  },
  components: {
  }
}
</script>

<style>
body{
  margin:0;
}
.container{
  display:flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
div{
  box-sizing:border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.menu{
  background: darkslateblue;
  padding:15px;
  border-radius: 5px;
}
.menu a{
  color : white;
  padding: 10px;
}
.black-bg{
  width:100%;
  height:100%;
  background: rgba(0,0,0,0.5);
  position:fixed;
  padding:20px;
}
.white-bg{
  position:relative;
  top: 50%;
  width:100%;
  background:white;
  border-radius:8px;
  padding:20px;
}
.content{
  width: 50%;
}
.content img{
  width: 100%;
}
</style>
