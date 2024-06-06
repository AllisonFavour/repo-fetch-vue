<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div>
    <h1>User View</h1>

    <RouterLink to="/profile">View Repo Details</RouterLink>

    <RouterView></RouterView>
  </div>
</template>
