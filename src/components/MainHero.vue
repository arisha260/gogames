<script setup>
  import Button from "@/components/MainButton.vue";
  import IconHero from "@/components/icons/IconHero.vue";
</script>

<template>
  <section class="hero">
    <div class="container hero__container grid">
      <div class="content hero__content">
        <h2 class="content__title title">Gaming Consoles</h2>
        <h3 class="content__subtitle subtitle">Try It, Rent It, <span style="color: var(--bismark-color)">Save $50!</span></h3>
        <p class="content__descr descr">It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters as opposed.</p>
        <Button class="content__button" text="Get Started Now"></Button>
        <div class="hero__icon">
          <IconHero />
        </div>
      </div>
      <div class="hero__scene hero-scene">
        <img class="hero-scene__hole" src="/hole.svg" alt="Hole"/>
        <div class="hero-scene__center">
          <img class="hero-scene__boy" src="/boy.svg" alt="boy">
          <img class="hero-scene__emo" src="/emo.svg" alt="boy">
        </div>
        <img class="hero-scene__top" src="/box-1.png" alt="box1">
        <img class="hero-scene__bottom" src="/box-2.png" alt="box2">
      </div>
    </div>
  </section>
</template>

<style scoped lang="scss">
  .hero{
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    padding-top: 145px;
    padding-bottom: 98px;
    background-image: url("/hero-bg.jpg");
    overflow: hidden;

    &__icon{
      position: absolute;
      left: 50%;
      bottom: -30%;
      width: 120px;
      height: 120px;
      svg{
        animation: rotating 10s infinite linear;
      }
    }
  }

  .hero-scene{
    position: relative;
    width: 100%;
    height: 100%;
    &__hole{
      position: absolute;
      bottom: 0;
      width: 100%;
      zoom: .84;
    }
    &__center{
      position: relative;
      z-index: 3;
      width: 100%;
    }
    &__boy{
      position: relative;
      z-index: 3;
      width: 100%;
      opacity: 0;
      animation: fadeIn 1s ease-out forwards;
    }
    &__emo {
      position: absolute;
      left: 5.2vw;
      top: 3vh;
      z-index: 2;
      opacity: 0;
      animation: appearIn 1s ease-out forwards;
      animation-delay: 1s;
    }
    &__top{
      position: absolute;
      left: -6vw;
      top: -20px;
      z-index: 4;
    }
    &__bottom{
      position: absolute;
      right: -6vw;
      bottom: -20px;
      z-index: 4;
    }
  }
</style>