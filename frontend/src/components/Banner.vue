<template>
  <div class="banner">
    <img :src="bannerImage" alt="Banner" class="banner-image" />
    <div class="banner-text">
      <h1>Muñecos de Tela</h1>
      <p>Encuentra los mejores muñecos de tela para tus pequeños.</p>
    </div>
  </div>
</template>

<script>
import bannerImage from '../assets/banner-imagen.webp';

export default {
  name: 'Banner',
  data() {
    return {
      bannerImage
    };
  }
}
</script>

<style scoped>
.banner {
  position: relative;
  text-align: center;
  color: white;
}
.banner-image {
  width: 100%;
  height: auto;
}
.banner-text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: rgba(0, 0, 0, 0.5);
  padding: 20px;
}
.banner-text h1 {
  margin: 0;
  font-size: 2.5rem;
}
.banner-text p {
  margin: 10px 0 0;
}
</style>
