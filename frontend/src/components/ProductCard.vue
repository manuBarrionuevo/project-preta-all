<template>
  <div class="product-card">
    <img :src="product.image" alt="product.name" class="product-image" />
    <h2 class="product-name">{{ product.name }}</h2>
    <p class="product-price">\${{ product.price }}</p>
    <button @click="addToCart">Add to Cart</button>
  </div>
</template>

<script>
export default {
  name: 'ProductCard',
  props: {
    product: Object,
  },
  methods: {
    addToCart() {
      this.$emit('add-to-cart', this.product);
    },
  },
}
</script>

<style scoped>
.product-card {
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 1rem;
  text-align: center;
  background-color: #fff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s;
}
.product-card:hover {
  transform: scale(1.05);
}
.product-image {
  max-width: 100%;
  height: auto;
  border-radius: 8px;
}
.product-name {
  font-size: 1.25rem;
  margin: 0.5rem 0;
}
.product-price {
  color: #b12704;
  font-size: 1rem;
}
button {
  background-color: #333;
  color: #fff;
  border: none;
  padding: 0.5rem 1rem;
  cursor: pointer;
  border-radius: 4px;
}
button:hover {
  background-color: #555;
}
</style>
