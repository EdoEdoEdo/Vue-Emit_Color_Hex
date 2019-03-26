<template>
  <div id="app">
    <img src="./assets/img/logo.png">
    <h1>{{ msg }}</h1>
    <h2>{{colorName}}</h2>
    <buttonComponent v-bind:hex="red" label="lollone" @BUTTON_CLICK="pickColor"></buttonComponent>
    <buttonComponent v-bind:hex="green" label="asdone" @BUTTON_CLICK="pickColor"></buttonComponent>
    <buttonComponent v-bind:hex="blue" label="patatone" @BUTTON_CLICK="pickColor"></buttonComponent>
  </div>
</template>

<script>

import buttonComponent from './components/button.vue';

export default {

  components:{
    buttonComponent
  },

  name: 'app',
  data () {
    return {
      msg: 'TEST COLORS',
      colorName: "select color",
      red:'#ff0000',
      green:'#00ff00',
      blue:'#0000ff'
    }
  },

  methods:{
    pickColor: function(payload){
      this.colorName = payload;
      console.log(payload)

    }
    
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
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

a {
  color: #42b983;
}
</style>
