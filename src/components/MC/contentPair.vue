<script setup>
defineProps({
  contentPairData: []
})
</script>


<template>
  <div class="inner-container">
    <div class="content">
      <div class="content-block">
        <span>
          <h2>{{ contentPairData.title }}</h2>
          <p>{{ contentPairData.description }}</p>
        </span>
        <span>
          <img v-for="image in contentPairData.imageList" :src="image.imageurl" alt="">
        </span>
      </div>
    </div>
  </div>
</template>

<style scoped>
.content-block {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 100px;
}

.content-block {
   align-items: center;
}

h2 {
  text-align: left;
}

span>img {
  border: 22px solid var(--brand-white);
  border-radius: 20px;
  box-shadow: -1px 1px 10px 1px rgb(219, 218, 218);
}

@media (max-width: 600px) {
  .content-block {
    grid-template-columns: repeat(1, 1fr);
  }
}

div>span {
  padding-right: 20px;
}
</style>