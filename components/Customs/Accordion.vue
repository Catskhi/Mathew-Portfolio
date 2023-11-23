<script setup lang="ts">

const props = defineProps<{
    resume_items: {
        label: string,
        content?: string,
        slot?: string
    }[]
}>()

</script>

<template>
<UAccordion :items="resume_items" >
    <template #item="{item}">
        <p>
            {{ item.content }}
        </p>
    </template>
    <template #experience-portfolio>
        <p>
            Over three years, I've developed as a graphic and web designer, gaining experience in freelancing, projects for fictitious entities, and collaborations with reputable companies, including my venture, IRoll.
            I have contributed to diverse platforms like Instagram, YouTube, and currently work with a prominent company. My portfolio highlights impactful collaborations with esteemed organizations.
            Explore these projects by <a class="font-bold text-white cursor-pointer hover:text-slate-300 transition-all duration-150">clicking here</a> to see my capability in delivering exceptional design solutions.
        </p>
    </template>
    <template #work-with-me>
        <p>
            For inquiries regarding potential collaborations or hiring opportunities, please feel free to reach out to me via the following channels:
            <br><br>
            Phone: +55 31 98527-7094
            <br><br>
            Email: <a href="mailto:matheusdesousacarvalho17@gmail.com" target="_blank" class="link">matheusdesousacarvalho17@gmail.com</a>
            <br><br>
            Behance: <a href="https://www.behance.net/matheuscarvalho121" target="_blank" class="link">https://www.behance.net/matheuscarvalho121</a>
        </p>
    </template>
    <template #default="{ item, index, open }">
        <UButton class="!bg-transparent !text-[#A8A8A8] border-b-[#555555] border-b py-3">
            <template #leading>
                <span class="text-base xl:text-lg">{{ item.label }}</span>
            </template>
            <template #trailing>
                <Icon
                    name="ri:arrow-drop-down-line"
                    class="text-3xl ms-auto text-[#00FFC2] transform transition-transform duration-200"
                    :class="[open && 'rotate-180']"
                />
            </template>
        </UButton>
    </template>
</UAccordion>
</template>

<style scoped>


p {
    @apply px-2 text-sm xl:text-base;
}

.link {
    @apply text-[#00FFC2] hover:text-[#2cb696] transition-all duration-150;
}

</style>