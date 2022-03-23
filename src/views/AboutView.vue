<template>
  <section class="about-section">
    <h1>About Me</h1>
    
    <div class="about-group">
      <div class="about-image">
        <img src="https://previews.123rf.com/images/apoev/apoev2107/apoev210700033/171405527-default-avatar-photo-placeholder-gray-profile-picture-icon-business-man-illustration.jpg" alt="">
      </div>
      <div class="about-text">
        <p>
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Saepe,
          velit odio? Fugiat ratione voluptatem, blanditiis itaque
          doloremque animi cupiditate assumenda, ad expedita vitae,
          reiciendis minima at nisi non eum cumque.
        </p>
        <br>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi
          aspernatur earum beatae at aperiam non molestias nam mollitia
          delectus corrupti itaque tempore ut facilis quidem dolor, iusto
          impedit consequatur! Similique?
        </p>
        <br>
        <p>
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quod,
          animi possimus provident quo doloremque aspernatur enim hic
          neque aperiam tempora molestiae vel tempore harum voluptatibus
          voluptatem molestias itaque voluptas alias?
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>

.about-section{
  width: 100vw;
}

.about-group{
  display: flex;
  align-items: center;
  justify-content: center;
  width: 90%;
  margin: 5%;
}

.about-image{
  width: 50%;
}

img{
  width: 100%;
  border-radius: 20px;
  border: hsla(160, 100%, 37%, 0.5) 5px groove;
}

.about-text{
  margin-left: 5%;
  max-width: 45%;
  text-align: justify;
}

</style>
