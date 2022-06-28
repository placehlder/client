<template>
  <div class="logincontainer">
    <div class="loginform">
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

h1 {
  display: flex;
  justify-content: center;
  font-weight: var(--font-weight-semibold);
  color: var(--dark-blue);
  font-size: var(--font-size-medium);
  margin-bottom: 2em;
  cursor: pointer;
}

input {
  color: var(--dark-blue);
  font-weight: var(--font-weight-medium);
  font-size: var(--font-size-small);
  padding: 1.4em 0em 1.4em 1.2em;
  width: 22em;
  border-style: none;
  border-radius: 0.3em;
  background-color: var(--light-grey);
  margin: 0em 0em 1.2em 0em;
  outline: none;
}

button {
  color: #3B4252;
  font-weight: var(--font-weight-semibold);
  font-size: var(--font-size-regular);
  width: 100%;
  background-color: var(--baby-blue);
  padding: 1.2em 0em 1.2em 0em;
  transition: background-color 0.2s ease-in-out;
  border-style: none;
  border-radius: 0.3em;
  margin-bottom: 0.8em;
  cursor: pointer;
}

.button:hover {
  background-color: var(--complete-white);
  color: var(--complete-black);
}

::placeholder {
  font-family: "Poppins", sans-serif;
  color: var(--medium-grey);
  font-weight: var(--font-weight-medium);
  font-size: var(--font-size-small);
}

::selection {
  background: var(--baby-blue);
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
  color: var(--dark-blue);
  font-weight: var(--font-weight-medium);
  font-size: var(--font-weight-small);
  padding-right: 1.5em;
}

.terms {
  text-decoration: none;
  color: var(--dark-blue);
  font-weight: var(--font-weight-small);
  font-size: var(--font-weight-small);
}

.github {
  text-decoration: none;
  color: var(--dark-blue);
  font-weight: var(--font-weight-small);
  font-size: var(--font-weight-small);
  padding-left: 1.5em;
}

</style>