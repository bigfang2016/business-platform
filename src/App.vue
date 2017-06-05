<template>
  <div id="app">
    <img src="./assets/logo.png">

    <router-view name="viewA"></router-view>
    <router-view name="viewB"></router-view>
    <router-view ></router-view>

    <router-link :to="{name:'foo1'}">go to foo</router-link>
    <router-link to="/bar">go to bar</router-link>
    <button @click="getParams">getParams</button>
  </div>
</template>

<script>
// import Hello from './components/Hello'

export default {
  name: 'app',
  components: {},
  methods:{
      getParams(){
          console.log(this.$route.params);
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
</style>
