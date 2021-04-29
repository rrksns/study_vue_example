<template>
 
<div class="menu" >
  <a v-for="(item,i) in menus" :key="i">{{item}}</a>
  
</div>

  <div>
    <img src="./assets/room0.jpg" alt="" class="room-img">
    <h4>{{products[0]}}</h4>
    <p>70만원</p>
    <button @click="addCnt">허위매물신고</button><span>신고수 : {{reportCnt[0]}}</span>    
  </div>

  <div>
    <img src="./assets/room1.jpg" alt="" class="room-img">
    <h4>{{products[1]}}</h4>
    <p>10만원</p>    
    <button @click="addCnt1">허위매물신고</button><span>신고수 : {{reportCnt[1]}}</span>
  </div>

  <div>
    <img src="./assets/room2.jpg" alt="" class="room-img">
    <h4>{{products[2]}}</h4>
    <p>xx만원</p>    
    <button @click="addCnt2">허위매물신고</button><span>신고수 : {{reportCnt[2]}}</span>
  </div>
  
</template>

<script>


export default {
  name: 'App',
  data(){
    return{
      price1 : 60,
      price2 : 70,
      reportCnt : [0,0,0],
      products : ['역삼동 원름','천호동 원룸','상계동 원룸'],
      menus: ['Home', 'Shop', 'About']
    }
  },
  components: {   
  },
  methods: {
    addCnt(){
      this.reportCnt[0]++
    },
    addCnt1(){
      this.reportCnt[1]++
    },
    addCnt2(){
      this.reportCnt[2]++
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  

}

.menu{
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;

}

.menu a{
  color: white;
  padding: 10px;
}

.room-img{
  width:100%;
  margin-top: 40px;
}
</style>
