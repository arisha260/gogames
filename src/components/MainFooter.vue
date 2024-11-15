<script setup>
  import Facebook from "@/components/icons/IconFacebook.vue";
  import Twitter from "@/components/icons/IconTwitter.vue";
  import Instagramm from "@/components/icons/IconInstagramm.vue";
</script>

<template>
  <footer class="footer">
    <div class="container footer__container">
      <img class="footer__logo" src="/logo.png" alt="site logo" width="238" height="65" />
      <div class="footer__copy">Copyright © 2022 HEALAS.LT. All Rights Reserved.</div>
      <ul class="list-reset footer__list">
        <li class="footer__item">
          <a href="#" class="footer__link"><Facebook/></a>
        </li>
        <li class="footer__item">
          <a href="#" class="footer__link"><Twitter/></a>
        </li>
        <li class="footer__item">
          <a href="#" class="footer__link"><Instagramm/></a>
        </li>
      </ul>
    </div>
  </footer>
</template>

<style scoped lang="scss">
  .footer{
    padding-top: 25px;
    padding-bottom: 20px;
    background-color: var(--beige-color);
    border-top: 1.50px solid #816f8c;;
    &__container{
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    &__copy{
      font-family: var(--font-family);
      font-size: 16px;
      color: var(--rum-color);
    }
    &__list{
      display: flex;
      gap: 18px;
      align-items: center;
    }
    &__link{
      display: flex;
      align-items: center;
      justify-content: center;
      width: 40px;
      height: 40px;
      padding: 10px;
      border-radius: 100%;
      box-shadow: -1px -1px 8px 0 rgba(255, 255, 255, 0.08);
      background: #fcd8cb;
      color: var(--bismark-color);
      transition: all 0.3s ease;
      @media (hover: hover) {
        &:hover{
          background-color: var(--bismark-color);
          color: var(--light-color);
        }
      }
      &:active{
        opacity: 0.5;
      }
    }
  }
</style>