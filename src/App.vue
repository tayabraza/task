<script setup>
  import { ref, onMounted } from 'vue';
  import { gsap } from 'gsap';
  import { ScrollTrigger } from 'gsap/ScrollTrigger';
  import Top from './components/TopComponent.vue';
  import Bottom from './components/BottomComponent.vue';
  import data from './assets/data.json';

  const fullYear = new Date().getFullYear();
  const blocks = ref(null);
  gsap.registerPlugin(ScrollTrigger);
  onMounted(() => {
    const tl = gsap.timeline({
      scrollTrigger: {
        trigger: blocks,
        start: 'top center',
        end: 'bottom bottom' 
      }
    });
    tl.fromTo(blocks, { opacity: 0, y: 0 },{ opacity: 1, y: 100, duration: 1 });
  });
  function reveal() {
    const reveals = document.querySelectorAll(".bottom-block");
    for (let i = 0; i < reveals.length; i++) {
      let elementTop = reveals[i].getBoundingClientRect().top;
      if (elementTop < window.innerHeight - 500) {
        reveals[i].classList.add("active");
      } else {
        reveals[i].classList.remove("active");
      }
    }
  }
  window.addEventListener("scroll", reveal);
</script>

<template>

  <header class="text-center">
    <h1>GET AHEAD</h1>
  </header>

  <main>
    <Top />
    <Bottom v-for=" (v, i) of data" :topText="v.topText" :middleText="v.middleText" :bottomText="v.bottomText" :key="i" />
  </main>

  <footer class="text-center">
    <p>Red Snapper &copy; {{ fullYear }} </p>
  </footer>

</template>

<style scoped>
  h1{
    margin: 5rem auto 2rem;
    font-size: 26px;
    font-weight: 700;
    font-style: normal;
    letter-spacing: 3.25px;
    color: #148FCF;
  }
</style>
