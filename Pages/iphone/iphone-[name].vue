<template>
  <div>
    <p>Iphone {{ name }}</p>
  </div>
</template>
<script setup>
const route = useRoute();
const name = computed(() => {
  return route.params.name.replaceAll("-", " ");
});
</script>
