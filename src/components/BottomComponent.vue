<script setup>
  defineProps({
    topText: {
      type: String,
      required: true
    },
    middleText: {
      type: String,
      required: true
    },
    bottomText: {
      type: String,
      required: true
    }
  });
</script>

<template>
  <div class="bottom-block">
    <p class="topText">{{ topText }}</p>
    <h2 class="middleText">{{ middleText }}</h2>
    <p class="bottomText">{{ bottomText }}</p>
  </div>
</template>

<style scoped>
  .topText{
    font-size: 26px;
    font-weight: 700;
    font-style: normal;
    letter-spacing: 3.25px;
    color: #63C1FF;
  }
  .middleText{
    font-size: 72px;
    font-weight: 700;
    font-style: normal;
    letter-spacing: 0px;
    line-height: 72px;
    color: #148FCF;
  }
  .bottomText{
    font-size: 36px;
    font-weight: 700;
    font-style: normal;
    letter-spacing: 0px;
    line-height: 52px;
    color: #25303B;
  }
  .bottom-block{
    position: relative;
    max-width: 900px;
    height: 100vh;
    margin: 3rem auto;
    padding: 1rem;
    transform: translateY(100px);
    transition: 1s all ease;
    opacity: 0;
  }

  .bottom-block.active{
    transform: translateY(0);
    opacity: 1;
  }

  @media screen and (max-width: 400px) {
    .topText{
      font-size: 22px;
    }
    .middleText{
      font-size: 60px;
    }
    .bottomText{
      font-size: 24px;
    }
  }
  
</style>
