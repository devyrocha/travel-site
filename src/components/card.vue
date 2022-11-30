<template>
  <div class="card">
    <img :src="listCard.imageUrl" alt="">
    <a :href="link">
      <p>{{ listCard.destino }}</p>
    </a>
  </div>
</template>

<script>
export default {
  props: {
    destino: String,
    imageUrl: String,
    link: String,
    listCard: [Object, Array]
  },
};
</script>

<style scoped>
a {
  text-decoration: none;
  color: black;
}
.card {
  width: 300px;
  height: 300px;
  background: #fff;
  border-radius: 10px;
  box-shadow: rgba(0, 0, 0, 0.15) 1.95px 1.95px 2.6px;
  cursor: pointer;
}

img {
  position: relative;
  width: 300px;
  height: 240px;
  border-radius: 10px 10px 0px 0px;
}

p {
  position: relative;
  bottom: 1.5rem;
  font-size: 23px;
  padding: 15px;
}
</style>