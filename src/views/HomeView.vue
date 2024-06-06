<script setup></script>

<template>
  <main>
    <div class="main-div">
      <h1>Welcome to Allison Favour's Space 🚀</h1>

      <RouterLink to="/repos">
        <button>Click to view repositories</button>
      </RouterLink>
    </div>
  </main>
</template>

<style scoped>
.main-div {
  width: 100%;
  margin: 100px auto 50px;
  padding: 0 20px;
  text-align: center;
}

h1 {
  /* font-size: 2rem; */
  font-size: calc(0.6rem + 2.5vw);
  margin-bottom: 30px;
}

button {
  background-color: hsl(0, 0%, 0%);
  color: hsl(0, 8%, 90%);
  padding: 10px 20px;
  border-radius: 8px;
  cursor: pointer;
}

button > a {
  font-size: 1rem;
  color: hsl(0, 8%, 90%);
}

button:hover {
  color: hsla(160, 100%, 37%, 1);
  box-shadow: 2px 2px 3px 2px rgba(0, 0, 0, 0.2);
  opacity: 0.9;
}
</style>
