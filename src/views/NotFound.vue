<template>
  <div class="container">
    <h1 class="header">404</h1>
    <p class="normal">How did we end up here?</p>
  </div>
</template>

<style scoped>
@import "../assets/base.css";
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  color: var(--dark-blue);
  cursor: default;
}
.header {
  font-size: 8em;
  transition: color 0.2s;
}
.header:hover {
  color: var(--baby-blue);
}
.normal {
  font-size: 1em;
}
</style>