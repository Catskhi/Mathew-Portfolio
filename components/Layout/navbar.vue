<script setup lang="ts">
import { useWindowScroll } from '@vueuse/core'

const props = defineProps<{
    main_screen: HTMLDivElement | null
}>()

const open_side_bar = ref<boolean>(false)
const { x, y} = useWindowScroll()

</script>

<template>
<header class="fixed z-20" ref="el">
    <nav 
        class="absolute text-white px-8 pt-3 z-10 flex items-center w-screen lg:px-44 transition-all duration-150"
        :class="[y < 30 ? '' : 'bg-black bg-opacity-50 backdrop-blur-sm']"
    >
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
                    <a target="_blank" href="https://discord.gg/jX7gKu8xEg">IROLL</a>
                </li>
                <li class="text-3xl">
                    <a target="_blank" href="https://www.behance.net/matheuscarvalho121">CHECK MY PORTFOLIO</a>
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