<template>
  <nav
    class="bg-purple-900 shadow-lg p-3 text-white text-lg flex justify-between"
  >
    <NuxtLink to="/">Home</NuxtLink>
    <NuxtLink to="/about">about</NuxtLink>
    <NuxtLink to="/iphone">iphone</NuxtLink>
    <NuxtLink to="/profile">profile</NuxtLink>
    <p>Cart ({{ cart.length }})</p>
  </nav>
</template>

<script setup>
const cart = useCart();
</script>
