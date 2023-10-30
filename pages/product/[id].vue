<template>
    <div class="container">
        <div class="sub-container">
            <div class="product-title">
                <h1>Product Detail</h1>
                <h1 class="product-name">{{ product.title }}</h1>
            </div>
            <div class="description">
                <p>{{ product.description }}</p>
            </div>
            <div>
                <img :src="product.thumbnail" alt="">
            </div>
        </div>
    </div>
</template>

<script setup>
    const id = useRoute().params.id
    const { data: product } = await useFetch('https://dummyjson.com/products/' + id)
</script>

<style scoped>
    .container {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        background-color: #f5f5f5;
    }

    .sub-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        background-color: #fff;
        padding: 2rem;
        border-radius: 10px;
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
    }

    .product-title {
        text-align: center;
        display: flex;
        flex-direction: column;
        gap: 1rem;
        margin-bottom: 2rem;
    }

    .product-name {
        color: rgb(83, 1, 246);
        font-size: 2rem;
        font-weight: bold;
    }

    .description {
        text-align: center;
        margin-bottom: 2rem;
    }

    img {
        max-width: 100%;
        height: auto;
        margin-bottom: 2rem;
    }
</style>