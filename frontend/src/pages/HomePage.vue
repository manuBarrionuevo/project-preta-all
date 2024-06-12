<template>
  <div>
    <Banner />
    <ProductList />
  </div>
</template>

<script>
import Banner from '../components/Banner.vue';
import ProductList from '../components/ProductList.vue';

export default {
  name: 'HomePage',
  components: {
    Banner,
    ProductList,
  },
}
</script>

<style scoped>
/* Estilos para la página de inicio */
</style>
