<script setup>
import { reactive, onMounted } from 'vue'

const state = reactive({
  apiData: null
})

onMounted(() => {
  fetch('https://api.github.com/users/AllisonFavour/repos')
    .then((res) => res.json())
    .then((data) => {
      console.log(data)
      state.apiData = data
    })
})
</script>

<template>
  <div class="repos">
    <h1>Allison Favour's Repos</h1>

    <!-- <p>{{ state.apiData }}</p> -->
    <p v-if="!state.apiData" class="loading">Loading...</p>

    <div class="repo">
      <ul v-for="repo in state.apiData" :key="repo.id" class="repo-box">
        <li><span class="title">Repo name:</span> {{ repo.name }}</li>
        <li><span class="title">Repo id:</span> {{ repo.id }}</li>
        <li><span class="title">Repo description:</span> {{ repo.description }}</li>
      </ul>
    </div>

    <!-- <RouterView></RouterView> -->
  </div>
</template>

<style scoped>
.repos {
  width: 100%;
  margin: 20px auto 100px;
  padding: 0 20px;
  text-align: center;
}

.repos h1 {
  /* width: max-content; */
  margin: 20px auto;
  font-size: calc(0.4rem + 2vw);
  text-align: center;
  text-wrap: wrap;
}

.loading {
  color: hsla(160, 100%, 37%, 1);
}

.repo {
  display: flex;
  flex-wrap: wrap;
}

.repo-box {
  width: 500px;
  background-color: hsl(0, 0%, 0%);
  /* background-color: hsla(160, 100%, 37%, 1); */
  color: white;
  /* flex: 1; */
  /* height: auto; */

  margin: 10px auto 10px;
  padding: 20px;
  border-radius: 10px;
}

.title {
  color: hsla(160, 100%, 37%, 1);
}
</style>

<!--   /* width: fit-content;
  min-width: 220px;
  max-width: 500px; */
  /* border-bottom: 1px solid red; */ -->
