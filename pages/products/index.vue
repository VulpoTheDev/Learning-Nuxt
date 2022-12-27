<template>
    <div class="page">
        <h2>PRODUCTS</h2>
        <div class="products-grid">
            <ProductCard v-for="(dataItem, dataIndex) in data" :key="dataIndex" :title="dataItem.title"
                :description="dataItem.description" :image="dataItem.image" :id="dataItem.id" />
        </div>
    </div>
</template>

<script setup lang="ts">
    import { Data } from '~~/src/types/productData';
    definePageMeta({
        layout: "products"
    })

    const data: Data[] = await useFetch(`${process.env.BACKEND_URL}/products`).data
</script>

<style lang="scss" scoped>
        .page {
            .products-grid {
                display: grid;
                grid-template-columns: repeat(3, minmax(0, 1fr));
                gap: 1rem;
            }
        }
</style>