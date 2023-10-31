<script setup>
// import { gsap } from "gsap"
// import { ScrollTrigger } from "gsap/ScrollTrigger"
// gsap.registerPlugin(ScrollTrigger)

// gsap.to(".c", {
//   //   ScrollTrigger: {
//   //     trigger: ".c",
//   //     toggleActions: "restart pause none none",
//   //   },
//   x: 400,
//   rotation: 360,
//   duration: 3,
// })

if (process.client) {
  //   window.addEventListener("keyup", props.close)
  window.addEventListener("scroll", function () {
    console.log("scrollY", scrollY)
    var scrollPos = scrollY
    var newWidth = scrollPos + 20
    console.log("newWidth", newWidth)
    this.document.querySelector(".home-title").style.width = newWidth + "%"
  })
}
</script>

<template>
  <div class="home-wrapper">
    <div class="home-container">
      <div
        class="home-title fixed w-1/2 h-full flex flex-col justify-center items-center backdrop-blur-md top-0 left-0"
      >
        <h1 class="text-2xl">Reading List</h1>
        <p class="font-thin">Project by Jeremy Kung</p>
        <div class="c">C SCROLL</div>
      </div>
    </div>
  </div>
</template>

<style lang="css" scoped>
* {
  margin: 0;
  padding: 0;
}
.home-wrapper {
  background-image: url("../assets/img/blaz-photo-zMRLZh40kms-unsplash.jpg");
  height: 200vh;
  background-size: cover;
  background-position: center;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
