<template>
    <div class="container">
      <h1 class="header">Log into Your Account</h1>
      <form>
        <input class="box" name="username" placeholder="Enter Username" /><br />
        <input :type="visibility" class="box" name="password" placeholder="Enter Password" /><br />
        <button class="submit">Log In</button>
      </form>
    </div>
    <div class="bar">
      <RouterLink class="tags" to="/register">Register</RouterLink>
      <a class="tags" href="https://github.com/placehlder" target="_blank">Terms of Service</a>
      <a class="tags" href="https://github.com/placehlder" target="_blank">Github</a>
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
  padding: 1.4em 0 1.4em 1.2em;
  width: 22em;
  border-style: none;
  border-radius: 0.3em;
  background-color: var(--light-grey);
  margin-bottom: 1.2em;
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
  padding: 1.2em 0 1.2em 0;
  border-style: none;
  border-radius: 0.3em;
  margin-bottom: 0.8em;
  cursor: pointer;
  transition: background-color 0.2s ease-in-out;
}

.submit:hover {
  background-color: var(--baby-green);
}

/* container */
.container {
  display: flex;
  flex-direction: column;
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

/* bottom bar items */
.tags {
  font-weight: var(--font-weight-semibold);
  font-size: var(--font-size-small);
  text-decoration: none;
  color: var(--dark-blue);
  margin-right: 1.5em;
}

/* media query */
@media (max-width: 1024px) {
  .header {
    font-size: var(--font-size-regular);
  }

  .box {
    width: 18em;
  }

  .submit {
    font-size: var(--font-size-small);
  }

  .tags {
    font-size: var(--font-size-even-smaller);
  }
}
</style>

<script>
export default {
  data() {
    return {
      visibility: "password"
    }
  }
}
</script>