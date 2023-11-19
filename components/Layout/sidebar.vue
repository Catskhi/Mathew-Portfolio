<script setup lang="ts">

const props = defineProps<{
    opened: boolean
}>()

defineEmits(['update:opened'])

</script>

<template>
<div 
:class="opened ? 'right-0' : '-right-full'"
class="w-72 h-screen bg-[#121212] fixed z-30 text-white transition-all duration-300">
    <div class="absolute right-5 top-3"
        @click="$emit('update:opened', false)"
    >
        <Icon name="ph:x" class="text-3xl font-bold hover:text-slate-300 cursor-pointer transition-all duration-150" />
    </div>
    <div class="px-10 pt-14">
        <ul class="flex text-lg flex-col space-y-3">
            <li>
                <a href="#about">ABOUT</a>
            </li>
            <li>
                <a href="#resume">RESUME</a>
            </li>
            <li>
                <a href="https://discord.gg/UfxbFKsM" target="_blank">IROLL</a>
            </li>
            <li>
                <a href="#resume">CHECK MY PORTFOLIO</a>
            </li>
        </ul>
    </div>
</div>
</template>