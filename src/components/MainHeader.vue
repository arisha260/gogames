<script setup>
  import Nav from './MainNav.vue'
</script>

<template>
  <header class="header">
    <div class="container header__container">
      <a href="#" class="header__logo">
        <img loading="lazy" src="/logo.png" alt="Site logo" width="280" height="78">
      </a>
      <Nav />
    </div>
  </header>
</template>

<style scoped lang="scss">
  .header{
    position: absolute;
    top: 0;
    padding: 10px 0;
    width: 100%;
    &__container {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    &__button{
      margin-left: 55px;
    }
  }
</style>