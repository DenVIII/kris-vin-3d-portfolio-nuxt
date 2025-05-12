<template>
  <NavBar />
  <main class="content">
    <router-view></router-view>
  </main>
  <footer-section></footer-section>
</template>

<style lang="scss">
@media (max-width: 500px) {
  .header {
    font-size: 1.5rem;
  }
}
</style>
