<script setup>
  import Nav from './MainNav.vue'
  import Button from "@/components/MainButton.vue";
</script>

<template>
  <header class="header">
    <div class="container header__container">
      <a href="#" class="header__logo">
        <img loading="lazy" src="/logo.png" alt="Site logo" width="280" height="78">
      </a>
      <Nav />
      <Button class="header__button"/>
    </div>
  </header>
</template>

<style scoped lang="scss">
  .header{
    position: absolute;
    padding: 10px 0;
    width: 100%;
    &__container {
      display: flex;
      flex-direction: row;
      align-items: center;
    }
    &__button{
      margin-left: 55px;
    }
  }
</style>