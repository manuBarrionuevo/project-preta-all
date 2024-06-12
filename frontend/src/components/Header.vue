<template>
  <header class="header">
    <img src="@/assets/logoPreta.webp" alt="Preta Logo" class="logo" />
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Shop</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: #fff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}
.logo {
  height: 60px;
}
nav ul {
  display: flex;
  list-style: none;
}
nav ul li {
  margin: 0 10px;
}
nav ul li a {
  text-decoration: none;
  color: #333;
  font-weight: bold;
}
</style>
