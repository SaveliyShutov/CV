<script setup lang="ts">
import gsap from "gsap"

onMounted(() => {
  gsap.from('.logo-text', {
    duration: 1,
    x: -500,
    ease: "sine.out",
  });
  gsap.from('.arrow', {
    duration: 1,
    x: 500
  });
})

</script>

<template>
  <div class="header bg-amber-200 h-screen">
    <h1 class="logo-text text-9xl pt-3 pl-3 unbounded-black">
      Hello world!
    </h1>
    <div class="size-10 box"></div>
  </div>
</template>

<style></style>