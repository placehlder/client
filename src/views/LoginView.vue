<template>
  <div class="container">
    <div>
      <h1 class="header">Log into Your Account</h1>
      <form hx-post="/login">
        <input class="box" name="username" placeholder="Enter Username" /><br />
        <input class="box" name="password" placeholder="Enter Password" /><br />
        <button class="submit">Log In</button>
      </form>
    </div>
    <div class="bar">
      <RouterLink class="tags" to="/register">Register</RouterLink>
      <h3 class="tags">Terms of Service</h3>
      <a
        class="tags"
        href="https://github.com/placehlder/client"
        target="_blank"
        >Github</a
      >
    </div>
  </div>
</template>

<style scoped>
@import "../assets/base.css";

/* highlighting */
::selection {
  background: var(--baby-blue);
}

/* title */
.header {
  display: flex;
  justify-content: center;
  font-weight: var(--font-weight-semibold);
  font-size: var(--font-size-medium);
  color: var(--dark-blue);
  margin-bottom: 2em;
  cursor: pointer;
}

/* input */
.box {
  font-family: "Poppins", sans-serif;
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

::placeholder {
  font-family: "Poppins", sans-serif;
  color: var(--medium-grey);
  font-weight: var(--font-weight-medium);
  font-size: var(--font-size-small);
}

/* submit button */
.submit {
  font-family: "Poppins", sans-serif;
  color: var(--dark-blue);
  font-weight: var(--font-weight-semibold);
  font-size: var(--font-size-regular);
  width: 100%;
  background-color: var(--baby-blue);
  padding: 1.2em 0em 1.2em 0em;
  border-style: none;
  border-radius: 0.3em;
  margin-bottom: 0.8em;
  cursor: pointer;
  transition: background-color 0.2s ease-in-out;
}

.submit:hover {
  background-color: var(--baby-purple);
}

/* container */
.container {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
}

/* bottom bar */
.bar {
  display: flex;
  position: fixed;
  bottom: 0;
  left: 0;
  padding-left: 2em;
  padding-bottom: 1em;
}

.tags {
  font-weight: var(--font-weight-semibold);
  font-size: var(--font-size-small);
  text-decoration: none;
  color: var(--dark-blue);
  margin-right: 1.5em;
}

@media (max-width: 1024px) {
  h1 {
    font-size: var(--font-size-regular);
  }
  input {
    width: 18em;
  }
  button {
    font-size: var(--font-size-small);
  }
  .bar {
    justify-content: center;
    left: 100;
  }
  .tags {
    font-size: var(--font-size-even-smaller);
  }
}
</style>
