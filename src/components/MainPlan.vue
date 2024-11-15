<script setup>
  import MainButton from "@/components/MainButton.vue";

  defineProps({
    name: Text,
    cost: Text,
  })
</script>

<template>
  <div class="plan">
    <h4 class="plan__name">{{ name }}</h4>
    <div class="plan__value">
      <span class="plan__valute">$</span>
      <span class="plan__value-digit">{{ cost }}.00</span>
       / Per Hour
    </div>
    <ul class="list-reset plan__list">
      <li class="plan__item">10 users included</li>
      <li class="plan__item">2 GB of storage</li>
      <li class="plan__item">Email support</li>
      <li class="plan__item">Help center access</li>
      <li class="plan__item">10 users included</li>
    </ul>
    <MainButton class="plan__button" text="Select This Plan"/>
  </div>
</template>

<style scoped lang="scss">
  .plan{
    padding: clamp(15px, 3vw, 46px);
    padding-top: 36px;
    border-radius: 20px;
    box-shadow: 0 20px 50px 0 rgba(132, 148, 205, 0.08);
    background: var(--cinderella-color);
    &--main{
      background: url('/union.png'), linear-gradient(180deg, #446381 0, #826f8c 100%);
      background-position: left bottom, center;
      background-size: 50%, cover;
      background-repeat: no-repeat;
      transform: scaleY(1.1);
    }
    &__name{
      margin: 0;
      margin-bottom: 33px;
      font-family: var(--font-family);
      font-weight: 700;
      font-size: 32px;
      color: var(--bismark-color);
    }
    &__value{
      margin-bottom: 26px;
      font-family: var(--font-family);
      font-weight: 700;
      color: var(--apricot-color);
    }
    &__valute{
      font-size: 27px;
    }
    &__value-digit{
      font-size: clamp(32px, 3.8vw, 50px);
    }
      &__list{
        margin-bottom: 46px;
      }
    &__item{
      padding-left: 20px;
      margin-bottom: 30px;
      font-family: var(--font-family);
      font-size: 18px;
      color: var(--rum-color);
      position: relative;
      &::before{
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        content: "";
        position: absolute;
        left: 0;
        top: 50%;
        width: 13px;
        height: 10px;
        background-image: url("/arrow.svg");
        transform: translateY(-50%);
      }
    }
    &__button{
      width: 100%;
    }
}

  .plan--main .plan__name, .plan--main .plan__item{
    color: var(--light-color);
  }
</style>