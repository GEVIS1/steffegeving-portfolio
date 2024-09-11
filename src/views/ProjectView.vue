<template>
  <div class="projects">
    <div v-for="n in 5">
      <h1>Project {{ n }}</h1>
      <p>In depth info about project {{ n }} coming here.</p>
      <img src="https://picsum.photos/100" width="100px" />
    </div>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .projects {
    min-height: 80vh;
    max-height: 80vh;
    display: flex;
    align-items: center;
    flex-direction: column;
    overflow: scroll;
  }
}
</style>
