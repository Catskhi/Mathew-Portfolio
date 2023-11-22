<script setup lang="ts">

const props = defineProps<{
    title: string
    description: string
}>()

</script>

<template>
<div class="text-white flex items-center px-5">
    <div class="h-full">
        <Icon name="icon-park-solid:graphic-design" class="text-5xl xl:text-7xl" />
    </div>
    <div class="ml-5">
        <p class="font-inter font-bold title">{{ title }}</p>
        <p class="text-[#A8A8A8] my-2  xl:my-5 subtitle">{{ description }}</p>
        <a class="text-[#00FFC2] cursor-pointer hover:text-[#0E9776] subtitle
             transition-all duration-150">
            Learn More
        </a>
    </div>
</div>
</template>

<style scoped>
.title {
    @apply text-lg xl:text-xl 2xl:text-2xl;
}

.subtitle {
    @apply text-base xl:text-lg 2xl:text-xl
}

</style>