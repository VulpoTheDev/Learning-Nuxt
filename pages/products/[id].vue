<template>
  <div class="page">
    <div class="image">
      <img :src="data.image" alt="" />
    </div>
    <div class="details">
      <h1>{{ data.title }}</h1>
      <p>{{ data.description }}</p>
      <div class="purchase">
        <h2 class="price">${{ data.price }}</h2>
        <button class="purchase-button">Add to Cart</button>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
  import { Data } from "~~/types/productData"
  const { id } = useRoute().params;
  const data: Data = useFetch(`${process.env.BACKEND_URL}/products/${id}`).data
  definePageMeta({
    layout: "products",
  });
</script>
<style lang="scss" scoped>
    .page {
      display: flex;
      gap: 5%;

      .image {
        flex-basis: 45%;

        img {
          width: 100%;
          height: 500px;
        }
      }

      .details {
        flex-basis: 45%
      }
      .purchase {
        .purchase-button {
          padding: 5px;
          border-radius: 5px;

        }
      }
    }
  </style>


