<script setup>
  import Plan from "@/components/MainPlan.vue";
</script>

<template>
  <section class="plans">
    <div class="container plans__container">
      <h2 class="title plans__title">Our Pricing</h2>
      <h3 class="subtitle plans__subtitle">Choose Your Plan</h3>
      <ul class="list-reset plans__list">
        <li class="plans__item"><Plan name="Basic" cost="50"/></li>
        <li class="plans__item"><Plan class="plan--main" name="Standard" cost="95"/></li>
        <li class="plans__item"><Plan name="Premium" cost="120"/></li>
      </ul>
    </div>
  </section>
</template>

<style scoped lang="scss">
  .plans{
    padding-top: 48px;
    padding-bottom: 120px;
    background-color: var(--beige-color);
    &__title{
      margin: 0 0 23px;
      text-align: center;
    }
    &__subtitle{
      margin: 0 0 128px;
      text-align: center;
    }
    &__list{
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: clamp(20px, 3vw, 40px);
    }
  }
</style>