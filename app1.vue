<template>
  <div>
    <NuxtPage />

    <LazyHomeWelcome v-if="page === 'home'" />
    <LazyCounter v-if="page === 'counter'" />
    <!-- <button @click="toggle">Toggle</button> -->
    <!-- <component :is="MyComponent" /> -->
  </div>
</template>

<script setup>
const page = ref("home");

function view(name) {
  page.value = name;
}
</script>
