<template>
<div class="wrapper">
	<div class="container">
		<h1 id="welcome">Welcome</h1>
		
		<div class="form" id="loginForm">
			<input type="text" placeholder="Username" v-model="username">
			<input type="password" placeholder="Password" v-model="password" >
			<button v-on:click="login()">Login</button>
		</div>
	</div>
	
	<ul class="bg-bubbles">
		<li></li>
		<li></li>
		<li></li>
		<li></li>
		<li></li>
		<li></li>
		<li></li>
		<li></li>
		<li></li>
		<li></li>
	</ul>
</div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
	data(){
		return{
			username:'',
			password:''
		}
	},
	methods:{
		login(){
			document.getElementById("loginForm").className = 'form fadeOut';
			document.getElementById("loginForm").style.visibility = 'hidden';
			// document.getElementById("welcome").style.transform = 'translateY(100px)';
			document.getElementById("welcome").className = 'form-success'
			console.log("login")
		}
	}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
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
