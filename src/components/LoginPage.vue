<script setup>

</script>

<template>
  <div class="logincontainer">
    <div class="login">
      <h1>Log into Your Account</h1>
      <form hx-post="/login">
        <input class="inputbox" name="username" placeholder="Enter Username"><br/>
        <input class="inputbox" name="password" placeholder="Enter Password"><br/>
        <button class="inputsubmit">Log In</button>
      </form>
    </div>
    <div class="bar">
      <RouterLink class="router" to="/register">Register</RouterLink>
      <h3 class="terms">Terms of Service</h3>
      <h3 class="github">Github</h3>
    </div>
  </div>
</template>

<style scoped>
@import "../assets/base.css";

:root {
  background-color: #fff;
}

h1 {
  display: flex;
  justify-content: center;
  font-weight: 600;
  color: #3B4252;
  font-size: 1.4em;
  margin-bottom: 2em;
  cursor: pointer;
}

input {
  font-family: "Poppins", sans-serif;
  color: #3B4252;
  font-weight: 500;
  font-size: 0.9em;
  padding: 1.4em 0em 1.4em 1.2em;
  width: 22em;
  border-style: none;
  border-radius: 0.3em;
  background-color: #F9F9F9;
  margin: 0em 0em 1.2em 0em;
  outline: none;
}

button {
  font-family: "Poppins", sans-serif;
  color: #3B4252;
  font-weight: 600;
  font-size: 1em;
  width: 100%;
  background-color: #ADD8E6;
  padding: 1.2em 0em 1.2em 0em;
  transition: background-color 0.2s ease-in-out;
  border-style: none;
  border-radius: 0.3em;
  margin-bottom: 0.8em;
  cursor: pointer;
}

.button:hover {
  background-color: #fff;
  color: #000;
}

::placeholder {
  font-family: "Poppins", sans-serif;
  color: #A8ACB9;
  font-weight: 500;
  font-size: 0.9em;
}

::selection {
  background: #ADD8E6;
}

.logincontainer {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;  
}

.bar {
  display: flex;
  position: fixed;
  bottom: 0;
  left: 0;
  padding-left: 2em;
  padding-bottom: 1em;
}

.router {
  text-decoration: none;
  color: #3B4252;
  font-weight: 500;
  font-size: 0.9em;
  padding-right: 1.5em;
}

.terms {
  text-decoration: none;
  color: #3B4252;
  font-weight: 500;
  font-size: 0.9em;
}

.github {
  text-decoration: none;
  color: #3B4252;
  font-weight: 500;
  font-size: 0.9em;
  padding-left: 1.5em;
}

</style>