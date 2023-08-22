<script setup>
  import Contacts from '../assets/Contacts.png';
  import Decisions from '../assets/Decisions.png';
  import Time from '../assets/Time.png';
  import Network from '../assets/Network.png';
  import Perspective from '../assets/Perspective.png';

</script>

<template>
  <div class="row">
    <div class="block">
      <img :src="Contacts" alt="Contacts">
      <h4>Make New Contacts</h4>
      <p>Thecosystems is all about people. Not data.</p>
    </div>
    <div class="block">
      <img :src="Decisions" alt="Decisions">
      <h4>Make Better Decisions</h4>
      <p>Understand your stakeholders and their needs.</p>
    </div>
    <div class="block">
      <img :src="Time" alt="Time">
      <h4>Stay Up to Date</h4>
      <p>Things change quickly.</p>
    </div>
  </div>
  <div class="row">
    <div class="block">
      <img :src="Network" alt="Network">
      <h4>Explore Professional Networks</h4>
      <p>Understand your stakeholders and their needs.</p>
    </div>
    <div class="block">
      <img :src="Perspective" alt="Perspective">
      <h4>Identify Hidden Opportunities</h4>
      <p>Open a new world of possibility and engagement. </p>
    </div>
  </div>
</template>

<style scoped>

  .row{
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    text-align: center;
  }
  .block{
    margin: 1.5rem;
    padding: 3.5rem;
    border: 1px solid #ccc;
  }

  .block > img {
    width: 120px;
  }

  .block > h4 {
    font-size: 26px;
    font-weight: 700;
    font-style: normal;
    letter-spacing: 0px;
    text-align: center;
    line-height: 40px;
    color: #25303B;
  }

  .block > p {
    font-size: 18px;
    font-weight: 400;
    font-style: normal;
    letter-spacing: 0px;
    text-align: center;
    line-height: 28px;
    color: #25303B;
  }

  @media screen and (min-width: 768px) {
    .row{
      flex-direction: row;
    }
    .block{
      width: 100%;
    }
  }

</style>