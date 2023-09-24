<template>
    <div>
      <ProductList :products="data.products.edges" />
    </div>
  </template>
  <script setup>
  const { data } = await useAsyncData("products", () =>
    GqlProducts({ first: 3 })
  );
  </script>
  