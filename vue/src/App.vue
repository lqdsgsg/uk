<template>
  <RouterView />
</template>

<script setup lang="ts">
import { RouterView } from "vue-router";

window.addEventListener("beforeunload", () => beforeunloadFn());
const beforeunloadFn = () => {
  const asyncRoutesMark: boolean = true;
  /* @ts-ignore */
  localStorage.setItem("asyncRoutesMark", asyncRoutesMark);
};
</script>

<style>
.html,
.body {
  width: 100vw;
  height: 100vh;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
img {
  width: 100%;
  height: 100%;
}
a {
  text-decoration: none;
}
</style>
