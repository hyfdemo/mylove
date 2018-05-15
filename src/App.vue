<template>
  <div id="app" @click='toggle'>
    <img class="bgm" src="./assets/音乐.png" @click="music">
    <audio src=""></audio>
    <components :is='currentC'></components>
  </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld'
import View1 from '@/components/View1'

export default {
  name: 'App',
  components:{
    HelloWorld,
    View1
  },
  data(){
    return {
        index:0,
        routes:[HelloWorld,View1]
    }
  },
  computed:{
    currentC(){
      return this.routes[this.index]
    }
  },
  methods:{
    music(){

    },
    toggle(){
      this.index++
    }
  }
}
</script>

<style>
html{
  font-size: 16px;
}
html,body{
  height: 100%;
}
body,div,p{
  margin:0;
  padding:0;
}
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: inherit;
  background:url('./assets/bg.jpg') no-repeat center;
}
#app>div{
  height: inherit;  
}
.bgm{
  width: 2rem;
  height: 2rem;
  position: fixed;
  right: 1rem;
  top: 1rem;
  animation: rotate 3s linear  infinite ;
}
@keyframes rotate {
  from {
    transform: rotate(0)
  }
  to {
    transform:rotate(360deg)
  }
}
</style>
