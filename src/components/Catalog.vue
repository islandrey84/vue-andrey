<script setup>
import ImgMobil from "@/assets/img/icon_mobile.png";
import axios from "axios";
import { onMounted, ref } from "vue";

// string
// number
// boolean
// null and undefined
// bigint and symbol

// object

// const pushCatalog = () => {
//   catalog.push({
//     name: "test",
//     img: ImgMobil,
//   });
// };

const catalog = ref([
  {
    name: "Телефоны и планшеты",
    img: ImgMobil,
  },
  {
    name: "Компьютеры и ноутбуки",
    img: ImgMobil,
  },
]);

// pushCatalog();
// pushCatalog();

console.log(catalog);

// setTimeout(() => {
//   console.log("123");
// }, 2000);

// setTimeout(() => {
//   console.log("345");
// }, 0);

onMounted(async () => {
  //{
  // completed: false;
  // id: 1;
  // title: "delectus aut autem";
  // userId: 1;
  //}

  const { data } = await axios.get(
    "https://jsonplaceholder.typicode.com/todos/1"
  );
  catalog.value.push({
    name: data.title,
    img: ImgMobil,
  });
  console.log(catalog.value);
});
</script>

<template>
  <div class="catalog">
    <div class="catalog__content">
      <div class="catalog__links">
        <a href="" v-for="c in catalog" :key="c.name">
          <img :src="c.img" alt="" />
          {{ c.name }}
        </a>
        <!-- <a href="">
          <img
            src="/Users/c/Desktop/vue-project/src/assets/img/icon computer.png"
            alt=""
          />
          Компьютеры и ноутбуки
        </a>
        <a href="">
          <img
            src="/Users/c/Desktop/vue-project/src/assets/img/icon_ office equipment.png"
            alt=""
          />
          Оргтехника и сети
        </a> -->
      </div>
      <div class="catalog__banners">
        <div class="main__banner">
          <img
            src="/Users/c/Desktop/vue-project/src/assets/img/slider.png"
            alt=""
          />
        </div>
        <div class="second__banner">
          <div>
            <img
              src="/Users/c/Desktop/vue-project/src/assets/img/card.png"
              alt=""
            />
          </div>
          <div>
            <img
              src="/Users/c/Desktop/vue-project/src/assets/img/card.png"
              alt=""
            />
          </div>
          <div>
            <img
              src="/Users/c/Desktop/vue-project/src/assets/img/card.png"
              alt=""
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.catalog {
}

img {
  width: 100%;
}
.catalog__content {
  display: flex;
  gap: 12px;
  max-width: 1920px;
  padding: 12px 8px;
  margin: 0 auto;

  //   display: grid;
  //   grid-template-columns: 200px 1fr;
}
.catalog__links {
  border: 1px solid black;
  padding: 12px;
  border-radius: 12px;

  a {
    margin: 0 0 20px;
    align-items: center;
    display: flex;
    text-decoration: none;
    color: black;
    &:hover {
      text-decoration: underline;
    }
    img {
      width: 24px;
    }
  }
}

.catalog__banners {
  flex: 0 1 100%;
}
</style>
