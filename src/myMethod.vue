<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div>
    <!-- <h1>{{ count }}</h1>
    <button v-on:click="addNumber(1)">증가</button>
    <button v-on:click="minusNumber">감소</button>
    <button v-on:mouseover="addNumber(10)">마우스오버10증가</button> -->
    <h2>{{ message }}</h2>
    <button @click="greeting">인사하기</button>
    <button v-on:click="sayGoodbye">작별하기</button>
    <div @click="getMousePosition" class="box"></div>
    <button @click="addNumber($event, 10)">10더하기</button>
    <button @click="addNumber($event, 100)">100더하기</button>
</div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data(){
    return {
      count : 0,
      message: ""
    };
  },
  methods: {
    addNumber(e, value){
      // this.count = this.count + value;
      e.pageX
      this.message = `마우스 좌표 ${e.pageX}와 더하기 ${value}는 ${e.pageX + value} 입니다.`
    },
    minusNumber(){
      console.log(this)
      this.count -= 1;
    },
    greeting(){
      this.message = "안녕하세요";
    },
    sayGoodbye(){
      this.message = "안녕히가세요";
    },
    getMousePosition(event){
      this.message = `마우스의 위치는 ${event.pageX}, ${event.pageY}입니다.`;
      console.log(event)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

button{
  width: 200px;
  height: 100px;
  font-size: 24px;
}

.box{
  width: 200px;
  height: 100px;
  background-color: salmon;
}



</style>
