<template>
    <nav>
        <h1 class="logo">Hello</h1>
        <NuxtLink to="/">Home</NuxtLink>
        <NuxtLink to="/about">About</NuxtLink>
        <NuxtLink to="/info">Info</NuxtLink>
        <NuxtLink to="/product">Product</NuxtLink>
    </nav>
    <div>
        <slot />
    </div>
</template>

<script setup>

</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Inter', sans-serif;
}
nav {
    margin:auto;
    padding: 10px 0;
    display: flex;
    justify-content: center;
    align-items: center;
    background: #333;
}
nav a {
    color: #fff;
    text-decoration: none;
    margin-left: 12px;
    font-size: 18px;
    padding: 10px;
}
nav a:hover {
    color: rgb(83, 1, 246);
}
.logo{
    color: rgb(83, 1, 246);
    margin-right: auto;
    font-size: 18px;
    padding-left: 10px;
}

</style>
