<template>
  <div>
    <Head>
      <Title>Nuxt 3 - Iphone {{ name }}</Title>
    </Head>
    <div class="flex justify-center w-full mt-20">
      <div class="grid grid-cols-2">
        <div>
          <img :src="`/images/iphone${route.params.name}.jpeg`" alt="" />
        </div>
        <div class="text-center">
          <h1 class="text-3xl">Iphone {{ name }}</h1>
          <button
            @click="addToCart()"
            class="p-3 bg-indigo-900 text-white rounded-md mt-5 w-48"
          >
            <span v-if="!isInCart()"> Add to cart </span>
            <span v-else> Remove from cart </span>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
const route = useRoute();

const name = computed(() => {
  return route.params.name.replaceAll("-", " ");
});

const fullName = computed(() => {
  return `Iphone-${route.params.name}`;
});
const cart = useCart();

function isInCart() {
  return !!cart.value.find((ct) => ct.name === fullName.value);
}

function addToCart() {
  if (!isInCart()) {
    cart.value.push({
      name: fullName.value,
    });
  } else {
    cart.value = cart.value.filter((ct) => ct.name !== fullName.value);
  }
}
// useHead({
//   title: `Nuxt 3 - Iphone ${route.params.name}`,
// });
</script>
