<script setup>

  defineProps({
    cards: Array
  })

</script>

<template>
  <div v-for='card in cards'>
    <img :src='card.photo' alt='pic'  />

    <div class='desc'>
      <div class='desc-top'>

        <div>
          <span v-show='card.superHost' class='superhost'>super host</span>
          <span class='type'>{{ card.type}} <span v-if='card.beds > 0'>. {{ card.beds }} beds</span></span>
        </div>

        <div>
          <span class='rating'>{{ card.rating }}</span>
        </div>

      </div>
      <p class='title'>{{ card.title}}</p>
    </div>

  </div>
</template>

<style scoped>
  img{
    max-inline-size: 100%;
    block-size: auto;
    border-radius: 15px;
  }

  .desc{
    margin-block-start: 1rem;
    font-weight: bold;
  }

  .desc-top{
    display: flex;
    justify-content: space-between;
  }

  .superhost{
    margin-inline-end: 0.5rem;
    border: 1px solid #4F4F4F;
    padding: 10px 20px;
    color: #4F4F4F;
    border-radius: 30px;
    text-transform: uppercase;
    font-size: 14px;
  }

  .type{
    color: #828282;
  }

  .title{
    font-size: 14px;
    margin-block-start: 1.5rem;
  }

  .rating{
    font-weight: normal;
  }

</style>
