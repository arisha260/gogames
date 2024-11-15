<script setup>

import Button from "@/components/MainButton.vue";
</script>

<template>
  <section class="vr-glasses">
    <div class="container vr-glasses__container grid">
      <div class="vr-glasses__scene vr-glasses-scene">
        <img class="vr-glasses-scene__screen" src="/screen.svg" alt="screen">
        <img class="vr-glasses-scene__men" src="/game-men.svg" alt="game men">
      </div>
      <div class="content vr-glasses__content">
        <h2 class="content__title title">About VR Glasses</h2>
        <h3 class="content__subtitle subtitle">The New VR Glasses Series</h3>
        <p class="content__descr descr">It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters as opposed.</p>
        <Button class="content__button" text="Get Started Now"></Button>
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
  .vr-glasses{
    background-image: url("/kerfin.png"), url("/vr-glasses-bg.jpg");
    background-position: top 50px right -27%, center;
    background-size: 35%, cover;
    background-repeat: no-repeat;
    &__container{
      padding-top: 60px;
      padding-bottom: 92px;
      background-image: url("/vr.png");
      background-repeat: no-repeat;
      background-position: bottom right 12%;
    }
  }

  .vr-glasses-scene{
    position: relative;
    &__men{
      position: relative;
      z-index: 3;
    }
    &__screen{
      position: absolute;
      right: 20px;
      top: 0;
      z-index: 2;
      zoom: .87;
      animation: flying 3.3s linear infinite;
    }
  }
</style>