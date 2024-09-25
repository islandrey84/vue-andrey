<script setup></script>

<template>
  <nav>
    <div class="nav__content">
      <div class="left__block">
        <a href="#" class="logo mobile"
          ><img
            src="/Users/c/Desktop/vue-project/src/assets/img/logo.png"
            alt=""
          />
        </a>

        <button class="button__catalog">
          <img
            src="/Users/c/Desktop/vue-project/src/assets/img/burger.png"
            alt=""
          />
          <span class="mobile">КАТАЛОГ</span>
        </button>
        <div class="search__bar">
          <label for="search" class="nav__search">
            <input
              id="search"
              type="text"
              placeholder="Поиск по сайту"
              required
            />
            <img
              src="/Users/c/Desktop/vue-project/src/assets/img/lens.png"
              alt=""
            />
          </label>
        </div>
      </div>

      <div class="right__block mobile">
        <a href="">
          <img
            src="/Users/c/Desktop/vue-project/src/assets/img/clock.png"
            alt=""
          />
          Статус заказа
        </a>
        <a href="">
          <img
            src="/Users/c/Desktop/vue-project/src/assets/img/graph.png"
            alt=""
          />
          Сравнение
        </a>
        <a href="">
          <img
            src="/Users/c/Desktop/vue-project/src/assets/img/heart.png"
            alt=""
          />
          Избранное
        </a>
        <a href="">
          <img
            src="/Users/c/Desktop/vue-project/src/assets/img/clock.png"
            alt=""
          />
          Статус заказа
        </a>
        <a href="">
          <img
            src="/Users/c/Desktop/vue-project/src/assets/img/basket.png"
            alt=""
          />
          324560Р
        </a>
        <a href="">
          <img
            src="/Users/c/Desktop/vue-project/src/assets/img/man.png"
            alt=""
          />
          Вход
        </a>
        <span>|</span>
        <a href=""> Регистрация </a>
      </div>
    </div>
  </nav>
</template>

<style scoped lang="scss">
nav {
  background-color: #ffff;
  box-shadow: 2px 2px 6px #00000010;
  // height: 59px;
}
.nav__content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1920px;
  padding: 12px 8px;
  margin: 0 auto;
}

.button__catalog {
  background-color: #ffee00;
  height: 40px;
  width: 135px;
  border-radius: 4px;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 4px;
  border-style: none;
  font-family: Rubik, "sans-serif";
}
.nav__search {
  border-style: none;
  border: 1px solid, #f2f2f2;
  color: #888b95;
}

.left__block {
  display: flex;
  gap: 10px;
  align-items: center;
  @media screen and (max-width: 1200px) {
    // flex-wrap: wrap;
    // margin-right: 100%;
    justify-content: space-between;
    width: 100%;
  }
}
.right__block {
  display: flex;
  gap: 10px;
  align-items: center;
  a {
    display: flex;
    gap: 5px;
    align-items: center;
    text-decoration: none;
    color: #000;
    &:hover {
      text-decoration: underline;
    }
  }
}
#search {
  border-style: none;
  outline-style: none;
  img {
    align-items: center;
  }
}

.mobile {
  @media screen and (max-width: 1200px) {
    display: none;
  }
}
</style>
