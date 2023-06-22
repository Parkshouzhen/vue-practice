<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div>
    <h1>Hello {{animal}}</h1>
    <h2>{{ food }}</h2>
    <h3 v-text="animal"></h3>
    <input type="text" v-model="food"/>
    <div>{{ alertMsg }}</div>
    <div v-html="alertMsg"></div>
    <div v-html="subscribeHTML"></div> <!--본인 코드/확실한 코드일 경우만 사용-->
    <img v-bind:src="imageSource" alt="random"/><br>
    <a v-bind:href="naverURL">naver</a><br>
    <a :href="daumURL">daum</a>
    <a :href="food">{{food}}</a> <!--food에 url 주소 넣어서 이동 가능-->
    <hr />
    <!--동적으로 클래스 부여하는 방법-->
    <h2 class="orange">원숭이는 {{ food }}를 좋아합니다.</h2>
    <h2 v-bind:class="{salmon: food==='orange', 'not-good': food==='rice'}">원숭이는 {{ food }}를 좋아합니다.</h2>
 </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data(){
    return {
      animal : "Monkey", //animal 변수를 template에서 연결 {{}}
      food : "banana", //단어가 바뀔 때마다 food로 연결된 모든 데이터가 업데이트 됨
      alertMsg : "<h2>경고입니다</h2>",
      //subscribeHTML : `<button onclick="document.querySelector('body').style.display='none'">구독하기</button>`
      imageSource : "https://placeimg.com/100/100/any",
      naverURL : "https://www.naver.com",
      daumURL : "https://www.daum.net"
    };
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

input{
  font-size: 20px;
}

.orange{
  color : orange;
}

.salmon{
  color : salmon;
}

.darkkhaki{
  color : darkkhaki;
}

.not-good{
  text-decoration : line-through;
}

</style>
