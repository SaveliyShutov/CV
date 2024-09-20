<script setup lang="ts">
import gsap from "gsap"

onMounted(() => {

  let rotate = gsap.timeline({
    scrollTrigger: {
      trigger: "#wrap",
      pin: true,
      scrub: 0.2,
      start: 'top top',
      end: '+=10000',
    }
  })
    .to('.arrow', {
      rotation: 870,
      duration: 1, ease: 'none',
    })
  gsap.to('.header', {
      duration: 1,
      rotationX: 45,
      scaleX: 0.8,
      z: -300,
    });


})

</script>
<template>
  <div>
    <h1 class="arrow text-9xl unbounded-black fixed right-5">V</h1>
    <Header />
    <Main />
  </div>


</template>
<style>
/* ::-webkit-scrollbar {
    display: none;
} */
body {
  min-height: 500vh;
}
</style>
