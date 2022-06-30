<template>
  <div class="container">
    <h1 class="header">404</h1>
    <p class="normal">How did we end up here?</p>
  </div>
</template>

<style scoped>
@import "../assets/base.css";

/* container */
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  color: var(--dark-blue);
  cursor: default;
}

/* 404 */
.header {
  font-size: 8em;
  transition: color 0.2s;
}
.header:hover {
  color: var(--baby-blue);
}

/* bottom text */
.normal {
  font-size: 1em;
}

@media (max-width: 1024px) {
  .header {
    font-size: 6em;
  }
}
</style>
