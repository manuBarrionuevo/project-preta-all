<template>
  <div class="product-list">
    <ProductCard 
      v-for="product in products" 
      :key="product.id" 
      :product="product"
      @add-to-cart="handleAddToCart"
    />
  </div>
</template>

<script>
import ProductCard from './ProductCard.vue';

export default {
  name: 'ProductList',
  components: {
    ProductCard,
  },
  data() {
    return {
      products: [
        { id: 1, name: 'Product 1', price: 10, image: 'https://via.placeholder.com/150' },
        { id: 2, name: 'Product 2', price: 20, image: 'https://via.placeholder.com/150' },
        { id: 3, name: 'Product 3', price: 30, image: 'https://via.placeholder.com/150' },
        { id: 4, name: 'Product 4', price: 40, image: 'https://via.placeholder.com/150' },
        { id: 5, name: 'Product 5', price: 50, image: 'https://via.placeholder.com/150' },
      ],
    };
  },
  methods: {
    handleAddToCart(product) {
      console.log('Producto añadido al carrito:', product);
    },
  },
}
</script>

<style scoped>
.product-list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 1rem;
  padding: 1rem;
}
</style>
