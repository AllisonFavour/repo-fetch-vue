<script setup>
// import {RouterLink}
</script>
<template>
  <div>
    <h1>404 Page</h1>

    <RouterLink to="/">
      <button class="home-btn">Back to home</button>
    </RouterLink>
  </div>
</template>

<style scoped>
div {
  width: 100%;
  margin: 50px auto;
  text-align: center;
}

h1 {
  font-size: calc(0.8rem + 2vw);
  color: hsla(160, 100%, 37%, 1);
  margin-bottom: 20px;
}

a {
  text-decoration: none;
  border: none;
}

.home-btn {
  background-color: hsla(160, 100%, 37%, 1);
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 10px;
  cursor: pointer;
}
</style>
