<template>
  <div id="app">
    <h1>HELLO</h1>
  <p>{{ email }}</p>
  <input type="text" v-model="email">
  <button @click="allertByEmail()">Wyswietl email</button>
  
  <div v-if="email.length < 10">Ale masz za krotki email</div>
  <div v-else-if="email.length < 15">Twoj email jest ok</div>
  <div v-else>Twoj email jest za dlugi!!!</div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  data(){
	  return {
		  email: "baaartek@onet.pl",
		  password: ""
	  };
  },
  methods: {
	  allertByEmail(){
		  alert(this.email);
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
