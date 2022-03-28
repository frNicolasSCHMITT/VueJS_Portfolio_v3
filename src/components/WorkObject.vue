<script>
export default{
  props: ['title', 'img', 'desc']
}
</script>

<template>
  <div class="card">
    <h3 class="card-title">{{ title }}</h3>
    <p class="card-desc">{{ desc }}
      <img class="card-img" :src="img" alt="">
    </p>
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
  position: relative;
  padding: 15px;
}

.card-img{
  z-index: -1;
  width: 100%;
  position: absolute;
  top: 0;
  right: 0;
  left: 0;
  bottom: 0;
}

.card:hover .card-desc{
  color: floralwhite;
}

.card:hover .card-img{
  opacity: 0.05;
}


</style>