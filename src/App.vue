<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import WorkInProgress from './components/WorkInProgress.vue'
</script>

<template>

  <WorkInProgress />

  <header>
    <div class="crop-image">
      <img alt="An image of me" class="logo" src="@/assets/me.jpg" />
    </div>

    <div class="wrapper">
      <HelloWorld msg="Hello World!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/projects">Projects</RouterLink>
        <RouterLink to="/cv">CV</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.crop-image {
  overflow: hidden;
  min-width: 200px;
  max-width: 200px;
  max-height: 200px;
  border-radius: 100%;
  margin: auto;
}
.logo {
  position: relative;
  left: -20px;
  display: block;
  object-fit: cover;
  width: 250px;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
  margin-bottom: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .crop-image {
    overflow: hidden;
    min-width: 200px;
    max-width: 200px;
    max-height: 200px;
    border-radius: 100%;
    margin-right: 3em;
  }
  .logo {
    position: relative;
    left: -20px;
    display: block;
    object-fit: cover;
    width: 250px;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    /* margin-left: -1rem; */
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
