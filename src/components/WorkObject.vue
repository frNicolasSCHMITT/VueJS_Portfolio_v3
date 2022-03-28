<script>
// defineProps({
//   works: {
//     title: String,
//     img: String,
//     desc: String,
//   }
// })
export default{
  props: ['title', 'img', 'desc']
}
</script>

<template>
  <div class="card">
    <h3 class="card-title">{{ title }}</h3>
    <p class="card-desc" :style="'background-image: url('+img+')' ">{{ desc }}</p>
  </div>
</template>

<style scoped>

.card{
  height: 300px;
  width: 400px;
  cursor: pointer;
}

.card-title{
  text-align: center;
  margin: 10px 0;
}

.card-desc{
  text-align: justify;
  width: 100%;
  height: 100%;
  color: transparent;
  background-size: contain;
  background-repeat: no-repeat;
}

.card:hover .card-desc{
  color: unset;
}


</style>