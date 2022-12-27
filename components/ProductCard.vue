<template>
  <div class="product">
    <NuxtLink :to="`/products/${id}`">
      <img :src="image" :alt="title">
      <h2>{{ title }}</h2>
      <div>
        {{ description }}
      </div>
    </NuxtLink>
  </div>
</template>

<script setup lang="ts">
  interface Props {
    title: string;
    description: string;
    image: string;
    id: number
  }

  const props = defineProps<Props>();
</script>
<style lang="scss" scoped>
    .product {
      display: flex;
      flex-direction: column;
      flex-basis: 20%;
      background: #111;
      box-shadow: 0 .5rem 1rem rgba(0, 0, 0, 0.15);
      padding: 1rem;
      border-radius: 1rem;
      font-size: 14px;

      img {
        margin: 20px 0;
        width: 50%;
        height: 50%;
      }
    }
  </style>
