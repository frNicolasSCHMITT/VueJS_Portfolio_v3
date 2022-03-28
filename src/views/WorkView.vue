<script>
import WorkObject from '@/components/WorkObject.vue'
// import WorkExample from '@/components/WorkExample.vue'
// import WorkObject_1 from '@/components/WorkObjects/WorkObject_1.vue'

export default {
  components: {
    WorkObject,
    // WorkExample,
    // WorkObject_1,
  },
  data() {
    return {
      works: [
        { 
          id: 1, 
          title: 'title: 1', 
          img: 'https://i0.wp.com/boingboing.net/wp-content/uploads/2016/03/OLD.jpg', 
          desc: 'description 1: Sort description of the website : Lorem ipsum dolor sit amet consectetur adipisicing elit. In ex quaerat animi, deleniti sequi labore corporis ut quidem et neque minima vel magni incidunt cupiditate sint nesciunt doloremque. Iste, sunt!' },
        {
          id: 2, 
          title: 'title: 2', 
          img: 'https://i0.wp.com/boingboing.net/wp-content/uploads/2016/03/OLD.jpg', 
          desc: 'description 2: Sort description of the website : Lorem ipsum dolor sit amet consectetur adipisicing elit. In ex quaerat animi, deleniti sequi labore corporis ut quidem et neque minima vel magni incidunt cupiditate sint nesciunt doloremque. Iste, sunt!' },
        { 
          id: 3, 
          title: 'title: 3', 
          img: 'https://i0.wp.com/boingboing.net/wp-content/uploads/2016/03/OLD.jpg', 
          desc: 'description 3: Sort description of the website : Lorem ipsum dolor sit amet consectetur adipisicing elit. In ex quaerat animi, deleniti sequi labore corporis ut quidem et neque minima vel magni incidunt cupiditate sint nesciunt doloremque. Iste, sunt!' },
        { 
          id: 4, 
          title: 'title: 4', 
          img: 'https://i0.wp.com/boingboing.net/wp-content/uploads/2016/03/OLD.jpg', 
          desc: 'description 4: Sort description of the website : Lorem ipsum dolor sit amet consectetur adipisicing elit. In ex quaerat animi, deleniti sequi labore corporis ut quidem et neque minima vel magni incidunt cupiditate sint nesciunt doloremque. Iste, sunt!' },
        { 
          id: 5, 
          title: 'title: 5', 
          img: 'https://i0.wp.com/boingboing.net/wp-content/uploads/2016/03/OLD.jpg', 
          desc: 'description 5: Sort description of the website : Lorem ipsum dolor sit amet consectetur adipisicing elit. In ex quaerat animi, deleniti sequi labore corporis ut quidem et neque minima vel magni incidunt cupiditate sint nesciunt doloremque. Iste, sunt!' }
      ]
    }
  }
}
</script>

<template>
  <h1>Some creations</h1>
  <section class="work-section">
    <div class="work-display">
      <div class="work-display-image"></div>
      <div class="work-display-text">
        <div class="work-display-name"></div>
        <div class="work-display-info"></div>
        <div class="work-display-link"></div>
      </div>
    </div>
    <div class="work-nav">
      <div class="work-object" 
        v-for="work in works"
        :key="work.id"
      >
      <WorkObject
        :title="work.title"
        :img="work.img"
        :desc="work.desc"
      />
      </div>
      <!-- <div class="work-object"><WorkExample /></div>
      <div class="work-object"><WorkExample /></div>
      <div class="work-object"><WorkExample /></div>
      <div class="work-object"><WorkExample /></div>
      <div class="work-object"><WorkExample /></div> -->
    </div>  
  </section>
</template>

<style>
.work-section{
  width: 100%;
  overflow: hidden;
}

.work-display{
  background-color: hsla(160, 100%, 37%, 0.5);
  height: 500px;
  width: 90%;
  margin: 0 5% 20px;
}

.work-nav{
  display: flex;
  width: 90%;
  margin: 0 5% 20px;
  overflow-x: auto;
  overflow-y: hidden;

  /* firefox */
  scrollbar-color: hsla(160, 100%, 37%, 1) hsla(160, 100%, 37%, 0.5);
  scrollbar-width: thin;
}

/* chrome */
.work-nav::-webkit-scrollbar{
  background-color: hsla(160, 100%, 37%, 0.5);
  height: 5px;
}
.work-nav::-webkit-scrollbar-thumb{
  background: hsla(160, 100%, 37%, 1);
}

.work-object{
  margin: 10px;
}

</style>
