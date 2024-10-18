<template>

  <nav class="navbar">
    <strong class="navbar__title">C.GG</strong>
  </nav>

  <section class="user__section">
    <div class="container">
      <div class="user__profile__info">
            <div class="user__profile__icon">
              <img class="user__icon" src="https://opgg-static.akamaized.net/meta/images/profile_icons/profileIcon6.jpg?image=e_upscale,q_auto:good,f_webp,w_auto&v=1729058249" alt="">
              <span class="level">804</span>
            </div>
        <div class="user__info">
          <div class="name__container">
            <strong class="user__nick">SKT Heclypso 어둠</strong>
            <span class="user__id">#HTML</span>
          </div>
            <ul class="team__and__rank">
              <li>
                <div class="region">
                  <img class="region__icon" src="https://s-lol-web.op.gg/assets/images/regions/01-icon-icon-br.svg?v=1729058249" alt="">
                  <span>BR</span>
                </div>
              </li>
            </ul>
            <q-btn @click="showInputContainer" class="update__info__btn">Atualizar dados</q-btn>
        </div>
      </div>
    </div>
  </section>

  <div v-if="isVisible" class="black__background">
    <div class="input__container">
      <h4>Insira a Matchup</h4>
      <input class="text__input" type="text">
      <q-btn @click="hideBackground"  class="close__input__container__button">X</q-btn>
    </div>
  </div>

  <section class="navegation__section">
    <div class="container">
    <div class="navegation__bar">
        <ul class="navegation__bar__list">
          <li class="navegation__bar__list__item--selected">
            <a href="#" class="navegation__bar__list__item__link">
              <div>Resumo</div>
            </a>
          </li>
          <li class="navegation__bar__list__item">
            <a href="#" class="navegation__bar__list__item__link">
              <div>Maestria</div>
            </a>
          </li>
          <li class="navegation__bar__list__item">
            <a href="#" class="navegation__bar__list__item__link">
              <div>Campeões</div>
            </a>
          </li>
          <li class="navegation__bar__list__item">
            <a href="#" class="navegation__bar__list__item__link">
              <div>Jogo ao Vivo</div>
            </a>
          </li>
        </ul>
      </div>
  </div>
  </section>

  <div class="container">
    <div class="banner">
      <img class="banner__image" src="https://servidor-estatico-alpha-six.vercel.app/brand-banner.jpg" alt="">
        <div class="text__container">
          <h2 class="banner__title">Tired of always taking a gap regardless of the matchup?</h2>
          <p class="banner__text">Download the app now and avoid it</p>
        </div>
      <q-btn class="banner__button">Download App</q-btn>
    </div>
  </div>

  <div class="content__container">
    <div class="left__content__container">

      <div class="left__content__header">Midlaner</div>
      <div class="left__content__body">Vladmir - High treat</div>

      <div class="left__content__header">Support</div>
      <div class="left__content__body">Blitzcrank - High treat</div>

    </div>

    <div class="main__content__container">
      <div class="main__content__header">Counter Itens</div>
      <div class="main__content__body">Da dodge porra</div>
      <q-btn class="view__more__button">View more</q-btn>
    </div>

  </div>

  <div class="container">
    <div class="announcement__container">
      container para anuncios
    </div>
  </div>

  <section class="footer__section">
    <div class="container">
      <div class="footer">

        <strong class="footer__title">C.GG</strong>

        <div class="footer__column">
            <strong class="footer__column__title">Title Placeholder</strong>
            <nav class="footer__column__nav">
              <a class="footer__column__link" href="#">Placeholder</a>
              <a class="footer__column__link" href="#">Placeholder</a>
              <a class="footer__column__link" href="#">Placeholder</a>
              <a class="footer__column__link" href="#">Placeholder</a>
            </nav>
        </div>

        <div class="footer__column">
            <strong class="footer__column__title">Title Placeholder</strong>
            <nav class="footer__column__nav">
              <a class="footer__column__link" href="#">Placeholder</a>
              <a class="footer__column__link" href="#">Placeholder</a>
              <a class="footer__column__link" href="#">Placeholder</a>
              <a class="footer__column__link" href="#">Placeholder</a>
            </nav>
        </div>

      </div>
    </div>
  </section>
</template> 
  
<script setup>
defineOptions({
  data() {
    return {
      isVisible: false,
    }
  }, 
  methods: {
    hideBackground() {
      this.isVisible = false;
    },

    showInputContainer() {
      this.isVisible = true;
    }
  }

});
</script>

<style>

  /* navbar */

  .navbar {
    background-color: #1c1c1f;
    height: 48px;
    display: flex;
    align-items: left;
    padding: 4px;
  }

  .navbar__title {
    font-size: 30px;
    color: #fff;
    margin-left: 20px;
  }

  /* header */

  .user__section {
    height: 228px;
    background-color: #31313c;
    position: relative;
  }
  
  .user__profile__info {
    padding: 50px 50px 16px 0;
    display: flex;
    position: absolute;
    z-index: 2;
  }

  .user__section::before {
    content: "";
    display: block;
    position: absolute;
    left: 50%;
    margin-left: -450px;
    width: 900px;
    top: 0;
    bottom: -45px;
    background: url(https://opgg-static.akamaized.net/meta/images/lol/latest/champion/centered/Brand_4.jpg?image=c_crop,w_1280,y_-120,x_0) no-repeat center center;
    -webkit-background-size: cover;
    background-size: cover;
    opacity: 0.4;
    z-index: 1;
  }

  .user__section::after {
    content: "";
    display: block;
    position: absolute;
    left: 50%;
    margin-left: -450px;
    width: 900px;
    top: 0;
    bottom: -45px;
    opacity: 1;
    background: url(https://s-lol-web.op.gg/static/images/site/summoner/mask_dark.svg) no-repeat center center;
    -webkit-background-size: cover;
    background-size: cover;
    z-index: 1;
  }

  .name__container {
    display: flex;
    gap: 4px;
  }

  .name__container,
  .team__and__rank {
    margin: 0px 0px 0px 24px;
  }

  .update__info__btn {
    margin: 10px 0px 0px 24px;
    background-color: #5383E8;
    color: #fff;
  }

  .user__profile__icon {
    position: relative;
  }

  .level {
    position: absolute;
    bottom: 0;
    left: 33%;
    background-color: #202d37;
    color: #fff;
    font-size: 12px;
    padding: 0 8px;
    border-radius: 10px;
  }

  .user__icon {
    width: 100px;
    height: 100px;
    border-radius: 20px
  }

  .user__nick {
    font-size: 24px;
    color: #fff
  }

  .user__id {
    font-size: 24px;
    color: #9e9eB1;
  }

  .region {
    font-size: 12px;
    display: flex;
    align-items: center;
    color: #9e9eB1;
    gap: 5px;
  }

  .region__icon {
    width: 16px;
    height: 16px
  }

  /* input */

  .input__container {
    position: absolute;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 500px;
    height: 400px;
    border-radius: 4px;
    background-color: #31313c;
    color: #fff;
    top: 20%;
    right: 40%;
    z-index: 5;
  }

  .close__input__container__button {
    position: absolute;
    top: 0;
    right: 0;
    background-color: red;
    color: #fff;
  }

  .black__background {
    position: absolute;
    top: 0;
    left: 0;
    z-index: 5;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.6);
    transition: 1s;
  }

  /* navegation section */

  .navegation__section {
    background-image: linear-gradient(to right,#31313c, #31313c, transparent, #31313c, #31313c );
    position: relative;
    z-index: 4; 
    padding: 4px 0;
    border-top: 1px solid;
    border-color: #ebeef1;
    border-color: #1C1C1F;
    margin-bottom: 8px;
  }

  .navegation__bar {
  }

  .navegation__bar__list {
    display: flex;
    gap: 8px;
    height: 36px;
  }

  .navegation__bar__list__item {
    font-size: 14px;
    padding: 8px 16px;
    min-width: 60px;
    border-radius: 4px;
  }

  .navegation__bar__list__item--selected {
    font-size: 14px;
    padding: 8px 16px;
    min-width: 60px;
    border-radius: 4px;
    background-color: #515163;
  }

  .navegation__bar__list__item:hover {
    background-color: #282830;
  }

  .navegation__bar__list__item__link {
    color: #fff;
  }

  /* banner */

  .banner {
    width: 1080px;
    height: 100px;
    position: relative;
    margin: 10px 0px 10px 0px;
  }

  .banner__image {
    border-radius: 4px
  }

  .text__container {
    position: absolute;
    top: 3%;
    left: 5%;
    line-height: 10px;
  }

  .banner__title {
    font-family: "Oswald", sans-serif;
    font-size: 28px;
    color: #fff;
    text-shadow: 1px 1px 0 #000;
    font-weight: 900;
  }

  .banner__text {
    font-family: "Roboto", sans-serif;
    font-size: 14px;
    color: #fff;
    text-shadow: 1px 1px 0 #000;
    font-weight: bold;
  }

  .banner__button {
    font-family: "Roboto", sans-serif;
    font-size: 14px;
    color: white;
    height: 33px;
    position: absolute;
    left: 84%;
    top: 33%;
    background-color: red;
  }

  /* content */

  .content__container {
    width: 1080px;
    display: grid;
    grid-template-columns: 1fr 2fr;
    gap: 8px;
    margin: 0 auto;
  }

  .left__content__container {

  }

  .left__content__header {
    width: 332px;
    height: 42.5px;
    background-color: #31313c;
    color: #fff;
    padding: 10px 0px 0px 15px;
    border-top-left-radius: 4px;
    border-top-right-radius: 4px;
    border-bottom: 1px solid;
    border-color: #1C1C1F;
  }

  .left__content__body {
    width: 332px;
    height: 122.5px;
    background-color: #31313c;
    color: #fff;
    padding: 10px 0px 0px 15px;
    border-bottom-left-radius: 4px;
    border-bottom-right-radius: 4px;
    margin-bottom: 8px;
  }

  .main__content__container {

  }

  .main__content__header {
    width: 740px;
    height: 42.5px;
    background-color: #31313c;
    color: #fff;
    padding: 10px 0px 0px 15px;
    border-top-left-radius: 4px;
    border-top-right-radius: 4px;
    border-bottom: 1px solid;
    border-color: #1C1C1F;
  }

  .main__content__body {
    width: 740px;
    height: 247.5px;
    background-color: #31313c;
    color: #fff;
    padding: 10px 0px 0px 15px;
    border-bottom-left-radius: 4px;
    border-bottom-right-radius: 4px;
    margin-bottom: 8px;
  }

  .view__more__button {
    width: 100%;
    height: 39px;
    background-color: #31313c;
    color: #fff;
  }

  /* annoncement */

  .announcement__container {
    width: 1080px;
    height: 250px;
    background-color: #31313c;
    color: #fff;
    margin-top: 400px;
  }

  /* footer */

  .footer__section {
    background-color: #31313c;
    padding: 5px;
    margin-top: 8px;
  }

  .footer {
    display: flex;
    justify-content: space-around;
    margin: 20px;
  }

  .footer__title {
    font-size: 40px;
    color: #d0d0dd;
  }

  .footer__column {
   
  }

  .footer__column__nav {
    display: flex;
    flex-direction: column;
    gap: 4px;
  }

  .footer__column__title {
    font-size: 14px;
    color: #fff
  }

  .footer__column__link {
    font-size: 14px;
    color: #9e9eB1
  }

</style>