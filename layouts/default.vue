<template>
    <header class="bg-background/75 backdrop-blur border-b -mb-px sticky top-0 z-50 border-primary-200/75 dark:border-primary-900/50">
        <div class="mx-auto px-4 sm:px-6 lgpx-8 max-w-7xl">
            <div class="flex items-center justify-between gap-3 h-[--header-height]">
                <div class="lg:flex-1 flex items-center gap-1.5">
                    <NuxtLink to="/" class="router-link-active router-link-exact-active flex items-end gap-1.5 font-bold text-xl text-gray-900 dark:text-white w-70">
                    <img src="../public/image/icon-green-square.png" alt="" class="w-[4rem] py-5">
                    </NuxtLink>
                </div>
                <ul class="gap-x-8 hidden lg:flex">
                    <li class="relative">
                        <NuxtLink to="/info" class="text-sm/6 font-semibold flex items-center gap-1 hover:text-primary">Info</NuxtLink>
                    </li>
                    <li class="relative">
                        <NuxtLink to="/info" class="text-sm/6 font-semibold flex items-center gap-1 hover:text-primary">Kuy</NuxtLink>
                    </li>
                    <li class="relative">
                        <NuxtLink to="/info" class="text-sm/6 font-semibold flex items-center gap-1 hover:text-primary">Documemt</NuxtLink>
                    </li>
                    <li class="relative">
                        <NuxtLink to="/info" class="text-sm/6 font-semibold flex items-center gap-1 hover:text-primary">Shop</NuxtLink>
                    </li>
                    <li class="relative">
                        <NuxtLink to="/info" class="text-sm/6 font-semibold flex items-center gap-1 hover:text-primary">About</NuxtLink>
                    </li>
                </ul>
                <div class="flex items-center justify-end lg:flex-1 gap-1.5">
                    <NuxtLink><img src="../public/image/github-icon-2048x1988-jzvzcf2t.png" alt="" class="w-[2rem]"></NuxtLink>
                </div>
            </div>
        </div>
    </header>
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
    font-weight: 600;
}
.logo{
    width: 60px;
}

</style>
