<script setup lang="ts">

const open_side_bar = ref<boolean>(false)

</script>

<template>
<header class="fixed z-20">
    <nav class="absolute text-white px-8 pt-3 z-10 flex items-center w-screen lg:px-44">
        <nuxt-icon name="Main_icon" filled class="text-[40px] lg:text-[75px]" />
        <ul class="font-tech flex justify-end w-full invisible xl:visible">
            <ul class="list-disc flex space-x-14">
                <li class="text-3xl">
                    <a href="#about">ABOUT</a>
                </li>
                <li class="text-3xl">
                    <a href="#resume">RESUME</a>
                </li>
                <li class="text-3xl">
                    <a href="#resume">IROLL</a>
                </li>
                <li class="text-3xl">
                    <a href="#resume">CHECK MY PORTFOLIO</a>
                </li>
            </ul>
        </ul>
        <div class="w-10 h-10 flex items-center justify-center cursor-pointer absolute right-8 hover:text-slate-300 transition-all duration-150 xl:invisible"
            @click="open_side_bar = !open_side_bar"
        >
            <Icon name="mingcute:menu-line" class="text-3xl" />
        </div>
    </nav>
    <LayoutSidebar v-model:opened="open_side_bar" />
</header>
</template>