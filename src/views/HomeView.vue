<script setup>
import TheWelcome from '@/components/TheWelcome.vue'
</script>

<template>
  <main>
    <div class="moon">
      <img src="src/assets/img/logoalphaNico.png" alt="logo">
    </div>
  </main>
</template>

<style>

@keyframes crescent {
  0% {
    transform: translate(-250px, 250px) scale(0.9);
    box-shadow: none;
  }
  50% {
    transform: translate(0px, 0px) scale(1.02);
    box-shadow: 0 0 10px #f9f3f2, 0 0 80px 8px #C7938B;
    background-color: #efdbd8;
  }
  100% {
    transform: translate(0px, 0px) scale(1.02);
    box-shadow: 0 0 10px #f9f3f2, 0 0 80px 8px #C7938B;
    background-color: #efdbd8;
  }
}

@keyframes crescent-mobile {
  0% {
    transform: translate(-100px, 100px) scale(0.9);
    box-shadow: none;
  }
  50% {
    transform: translate(0px, 0px) scale(1.02);
    box-shadow: 0 0 10px #f9f3f2, 0 0 80px 8px #C7938B;
    background-color: #efdbd8;
  }
  100% {
    transform: translate(0px, 0px) scale(1.02);
    box-shadow: 0 0 10px #f9f3f2, 0 0 80px 8px #C7938B;
    background-color: #efdbd8;
  }
}

@keyframes reveal {
  0% {
    opacity: 0;
    mix-blend-mode: overlay;
  }
  50% {
    opacity: 50%;
  }
  65% {
    /* opacity: 50%; */
  }
  100% {
    opacity: 100%;
    mix-blend-mode: normal;
  }
}

main {
  display: flex;
  justify-content: center;
  align-items: center;
  /* background-image: linear-gradient(30deg, #182C51, #09101e); */
  overflow: hidden;
  height: 90vh;
  z-index: -2;
}

.moon {
  /* background-image: linear-gradient(30deg, #13223f, #0e1a30); */
  width: 500px;
  height: 500px;
  border-radius: 50%;
  position: relative;
}
.moon::before {
  content: "";
  background-color: #C7938B;
  position: absolute;
  display: block;
  height: 100%;
  width: 100%;
  border-radius: 50%;
  z-index: -1;
  animation: 4s crescent linear infinite alternate;
}

.moon img {
  width: 100%;
  height: 100%;
  /* mix-blend-mode: overlay; */
  animation: 4s reveal linear infinite alternate;
}

@media (max-width: 992px) {
  .moon {
    width: 250px;
    height: 250px;
  }
  .moon::before {
    animation: 5s crescent-mobile linear infinite alternate;
  }
}

@media (max-width: 768px) {
  .moon {
    width: 160px;
    height: 160px;
  }
}
</style>