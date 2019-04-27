<template>
 <div id="app">
    <div v-if="loginPage == false">
      Zalogowano {{email}}
      <button @click="login()">Wroc</button>
    </div>
    <div v-else>
      <h1>LOGOWANIE</h1>
      Zaloguj sie:
      <input type="text" v-model="email">

      <button @click="login()">Zaloguj</button>
    </div>
  </div>
</template>

<script>
import "milligram";

export default {
  data(){
	  return {
		  email: "baaartek@onet.pl",
		  loginPage: true
	  };
  },
  methods: {
	  login(){
		  this.loginPage = this.loginPage === false;
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
