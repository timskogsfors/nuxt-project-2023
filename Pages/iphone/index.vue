<template>
  <div class="grid grid-cols-4 gap-4">
    <nuxt-link
      to="/iphone/iphone-12"
      class="shadow-lg border rounded-lg text-center"
    >
      <h1>Iphone 12</h1>
      <div class="flex justify-center">
        <img width="200" src="/images/iphone12.jpeg" alt="" />
      </div>
    </nuxt-link>
    <nuxt-link
      to="/iphone/iphone-14"
      class="shadow-lg border rounded-lg text-center"
    >
      <h1>Iphone 14</h1>
      <div class="flex justify-center">
        <img width="200" src="/images/iphone14.jpeg" alt="" />
      </div>
    </nuxt-link>
  </div>
</template>
<script setup>
useHead({
  title: "Nuxt 3 - Iphones",
  //   meta: [
  //     {
  //       hid: "description",
  //       name: "description",
  //       content: "Iphone 12",
  //     },
  //   ],
});
</script>
