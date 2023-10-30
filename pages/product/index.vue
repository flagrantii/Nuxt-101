<template>
        <div class="productlist">
                <div v-for="product in products.products">
                        <NuxtLink :to="`/product/${product.id}`"><h2 class="title">{{ product.title }}</h2></NuxtLink>
                        <p class="description">{{ product.description }}</p>
                        <img :src="product.thumbnail" alt="">
                </div>
        </div>
</template>

<script setup>
const {data : products} = await useFetch('https://dummyjson.com/products?limit=10')
console.log(products)
</script>

<style scoped>
.productlist {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}
.productlist div {
    width: 300px;
    height: 300px;
    margin: 30px 15px;
    background: #333;
}
.productlist div:hover{
    background: rgb(83, 1, 246);
}

.title{
    color: white;
    text-align: center;
    font-size: 1.2em;
}
.description{
    color: white;
    text-align: center;
    font-size: 0.6em;
}
img{
    width: 100%;
    height: 300px;
}
a{
    text-decoration: none;
}
</style>