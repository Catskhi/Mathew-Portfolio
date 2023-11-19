<script setup lang="ts">

const props = defineProps<{
    title: string
}>()

const show_text = ref<boolean>(false)

</script>

<template>
<div :class="[show_text ? '' : 'overflow-hidden']" class="w-full transition-all duration-150">
    <button class="border-b border-[#555555] text-[#A8A8A8] w-full text-left pb-3 relative"
        @click="show_text = !show_text"
    >
        {{ title }}
        <span class="absolute right-2 text-xl">
            +
        </span>
    </button>
    <p class="transition-all duration-150 mt-2 text-[#A8A8A8]" :class="[show_text ? 'block' : 'hidden']">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat, magnam facere vel nemo eius magni sit reiciendis explicabo eligendi earum ipsam minus delectus voluptates corporis impedit, consectetur expedita harum cupiditate?
    </p>
</div>
</template>