<script lang="ts" setup>
const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  price: {
    type: String,
    required: true,
  },
  image: {
    type: String,
    required: true,
  },
  link: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <div>
   <div>
    <NuxtLink :to="link">
      <img :src="image">
    </NuxtLink>
    <div> 
      <h5>{{ title }}</h5>
      <pre class="text-gray-500 mb-4">{{ price }}</pre>
      <p>{{ description }}</p>
    </div>
   </div>
  </div>
</template>


