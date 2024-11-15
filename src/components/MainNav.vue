<script setup>
  import Button from "@/components/MainButton.vue";
</script>

<template>
  <nav class="nav">
    <ul class="list-reset nav__list">
      <li class="nav__item"><a href="#" class="nav__link">Home</a></li>
      <li class="nav__item"><a href="#" class="nav__link">About Us</a></li>
      <li class="nav__item"><a href="#" class="nav__link">Prices</a></li>
      <li class="nav__item"><a href="#" class="nav__link">Rules</a></li>
    </ul>
    <Button class="header__button" text="Get Started Now"/>
  </nav>
</template>

<style scoped lang="scss">
  .nav{
    display: flex;
    align-items: center;
    &__list{
      margin-right: 55px;
      display: flex;
      gap: 46px;
    }
    &__link{
      font-family: var(--font-family);
      font-weight: 500;
      font-size: 18px;
      line-height: 133%;
      color: var(--bismark-color);
      transition: color .2s ease;
      position: relative;
      @media (hover: hover) {
        &:hover::after {
          width: 100%; // полная ширина при наведении
        }
      }
      &:active{
        color: var(--apricot-color);
      }
      &::after {
        content: "";
        position: absolute;
        left: 0;
        bottom: -2px; // отступ от текста
        width: 0; // изначальная ширина 0 для анимации слева направо
        height: 2px; // толщина линии подчеркивания
        background-color: var(--bismark-color); // цвет подчеркивания
        transition: width 0.3s ease; // плавное увеличение ширины
      }
    }
  }
</style>