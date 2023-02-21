<template>
  <div>
    <div>{{ product.title }}</div>
    <div>{{ product.price }}</div>
    <div>{{ product.id }}</div>
  </div>
</template>

<script setup>
const { id } = useRoute().params
const uri    = 'https://fakestoreapi.com/products/' + id
const { data: product } = await useFetch(uri, { key: id })

definePageMeta({
  layout: 'products'
})

</script>

<style scoped>

</style>