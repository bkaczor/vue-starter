<template>
 <div id="app">
    <div v-if="loginPage == false">
      <label>Zalogowano {{email}}</label>
      <button @click="loginSite()">Wroc</button>
    </div>
    <div v-else>
      <login-form @login="logMeIn($event)"></login-form>
    </div>
  </div>
</template>

<script>
import "milligram";
import LoginForm from "./LoginForm";

export default {
  components: {LoginForm},
  data(){
	  return {
		  loginPage: true,
		  email: "baaartek@onet.pl"
	  };
  },
  methods: {
	  loginSite(){
		  this.loginPage = true;
	  },
	  logMeIn(username) {
		  this.email = username;
		  this.loginPage = false;
		}
  } 
};
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
