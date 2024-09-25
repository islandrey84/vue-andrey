<script setup></script>

<template>
  <header>
    <div class="header__content mobile">
      <a href="#" class="logo"
        ><img
          src="/Users/c/Desktop/vue-project/src/assets/img/logo.png"
          alt=""
        />
      </a>
      <a href="" class="link__flex">
        Компания
        <img
          src="/Users/c/Desktop/vue-project/src/assets/img/Vector 2.png"
          alt=""
        />
      </a>
    </div>
    <div class="header__content desktop">
      <div class="header__links">
        <a href="#">
          <img
            src="/Users/c/Desktop/vue-project/src/assets/img/location.png"
            alt=""
          />
          Красноярск
        </a>
        <a href="">Магазины</a>
        <a href="">
          Покупателям
          <img
            src="/Users/c/Desktop/vue-project/src/assets/img/Vector 2.png"
            alt=""
          />
        </a>
        <a href="" class="link__flex">
          Компания
          <img
            src="/Users/c/Desktop/vue-project/src/assets/img/Vector 2.png"
            alt=""
          />
        </a>
        <a href="">
          Организациям
          <img
            src="/Users/c/Desktop/vue-project/src/assets/img/Vector 2.png"
            alt=""
          />
        </a>
        <a href="">Акции</a>
        <a href="">Статьи</a>
        <a href="">Подарочные карты</a>
      </div>
      <div class="header__phone">
        8 (800) 775-00-70 доб. 3020
        <span style="color: #c7c9d0">(бесплатно по России)</span>
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss">
header {
  /* display: flex;
  justify-content: center;
  align-items: center; */
  background-color: var(--bgGray);
}

.header__content {
  max-width: 1920px;
  padding: 0 8px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 44px;
  color: #fff;
  /* rem */
}

.header__links {
  display: flex;
  align-items: center;
  gap: 12px;
  a {
    color: #fff;
    text-decoration: none;
    display: flex;
    align-items: center;
    gap: 4px;

    &:hover {
      text-decoration: underline;
    }
  }
}

.mobile {
  display: none;
  @media screen and (max-width: 1400px) {
    display: flex;
  }
}

.desktop {
  display: flex;
  @media screen and (max-width: 1400px) {
    display: none;
  }
}
</style>
