<script setup>
import Header from "@/components/Header.vue";
import Nav from "@/components/Nav.vue";
import Catalog from "./components/Catalog.vue";
</script>

<template>
  <Header />
  <Nav />
  <Catalog />
</template>

<style scoped lang="scss">
.three {
  grid-column: 6;
  grid-row: 2;
}
</style>
