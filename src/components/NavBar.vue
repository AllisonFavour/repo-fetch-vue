<template>
  <nav>
    <div class="nav-bar">
      <div class="img-div">
        <img src="./images/github-logo.png" alt="" />
      </div>

      <div>
        <RouterLink to="/" class="nav-link">Home</RouterLink>
        <RouterLink to="/repos" class="nav-link">View Repos</RouterLink>
        <!-- <RouterLink to="/user" class="nav-link">User</RouterLink> -->
      </div>
    </div>
  </nav>
</template>

<style scoped>
.nav-bar {
  width: 100%;
  /* height: 14vh; */
  height: auto;
  padding: 14px 50px;
  display: flex;
  justify-content: space-between;
  place-items: center;
  align-items: center;
}

.nav-bar a {
  /* font-size: 1.6rem; */
  padding-left: 1rem;
}

.nav-bar a:nth-of-type(2) {
  border-left: 1px solid hsl(0, 0%, 0%);
  margin-left: 1rem;
}

.nav-bar a.router-link-exact-active {
  color: hsla(160, 100%, 37%, 1);
}

.img-div {
  width: 60px;
  height: auto;
}

img {
  max-width: 100%;
  height: auto;
}

div.nav-link {
  font-size: calc(0.2rem + 2vw);
}
</style>
