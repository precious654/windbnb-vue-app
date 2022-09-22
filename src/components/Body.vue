<script setup>
  import stay from '../stays.json';
  import Card from './Card.vue';

  console.log( stay );
</script>

<template>
  <div>
    <div class='top'>
      <h1>Stays in Finland</h1>
      <p>12+ stays</p>
    </div>
    <div class='body'>
      <Card :cards='stay' />
    </div>
  </div>
</template>

<style scoped>

  .top{
    display: flex;
    justify-content: space-between;
  }

  .top h1{
    font-weight: bolder;
  }

  .body{
    margin-block-start: 2rem;
    display: grid;
    grid-gap: 2rem;
    grid-template-columns: repeat(3, 1fr);
  }

</style>
