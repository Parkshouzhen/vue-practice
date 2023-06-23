<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div>
    <h1>{{ count }}</h1>
    <button v-on:click="addNumber(1)">증가</button>
    <button v-on:click="minusNumber">감소</button>
    <button v-on:mouseover="addNumber(10)">마우스오버10증가</button>
    <h2>안녕</h2>
</div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data(){
    return {
      count : 0
    };
  },
  methods: {
    addNumber(value){
      this.count = this.count + value;
    },
    minusNumber(){
      console.log(this)
      this.count -= 1;
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



</style>
