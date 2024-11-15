<script setup>

import IconHero from "@/components/icons/IconHero.vue";
import Button from "@/components/MainButton.vue";
</script>

<template>
  <section class="about-consoles">
    <div class="container about-consoles__container grid">
      <div class="content hero__content">
        <h2 class="content__title title">About XBOX, PS</h2>
        <h3 class="content__subtitle subtitle">The New Xbox, Ps Series</h3>
        <p class="content__descr descr">It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters as opposed.</p>
        <Button class="content__button" text="Get Started Now"></Button>
      </div>
      <div class="about-consoles__scene about-consoles-scene">
        <div class="about-consoles-scene__mecha">
          <img src="/mecha.svg" alt="mechanism">
        </div>
        <div class="about-consoles-scene__small-mecha">
          <img src="/small-mecha.svg" alt="small mechanism">
        </div>
        <img class="about-consoles-scene__gamepad" src="/game-pad.svg" alt="game pad">
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
  .about-consoles{
    padding-top: 29px;
    padding-bottom: 92px;
    background-image: url("/about-console-bg.jpg");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }

  .about-consoles-scene{
    position: relative;
    &__mecha{
      position: absolute;
      right: 16%;
      top: 0;
      z-index: 8;
      animation: rotating 10s linear infinite reverse;
    }
    &__small-mecha{
      position: absolute;
      right: 35%;
      top: 20%;
      z-index: 8;
      animation: rotating 10s linear infinite reverse;
    }
    &__gamepad{
      position: relative;
    }
  }
</style>