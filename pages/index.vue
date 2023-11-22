<script setup lang="ts">
const resume_items = [
    {
        label: 'About me and my graduation',
        content: "Self-made designer and lifelong learner. I've harnessed the power of self-education, crafting my skills through free online resources, in-depth research, and innovative thinking. My journey epitomizes self-reliance, transforming a passion for design into a profession, driven by an unwavering commitment to excellence. In this ever-evolving design landscape, I've journeyed alone, absorbing knowledge from YouTube courses, devouring online articles, and embracing curiosity. ",
        defaultOpen: true
    },
    {
        label: 'Experience and porfolio',
        slot: 'experience-portfolio'
    },
    {
        label: 'Work with me',
        slot: 'work-with-me'
    }
]

const main_screen = ref<HTMLDivElement | null>(null)
</script>

<template>
<main>
    <LayoutNavbar :main_screen="main_screen" />
    <div class="bg-[url('/Background_image.png')] h-screen w-screen bg-cover bg-center bg-no-repeat absolute" />
    <div class="h-screen w-creen grey_gradient"></div>
    <div ref="main_screen" class="lg:px-40 absolute top-0 w-screen flex">
        <div class="min-1/2 h-screen text-white z-10 flex flex-col justify-center pl-8">
            <p class="font-inter text-xl lg:text-2xl font-semibold">Simpler as f***</p>
            <h1 class="text-[50px] lg:text-[60px] font-extrabold">
                MATHEUS
                <span class="mt-5">CARVALHO</span>
            </h1>
            <p class="mt-5 lg:text-lg whitespace-nowrap">
                Simplicity is Elegance - Minimalist Design
                <br> by Matheus Carvalho
            </p>
            <a class="bg-[#E6E6E6] text-black font-inter mt-8 py-2 rounded text-left px-5 cursor-pointer hover:brightness-75 active:scale-[99%] transition-all duration-300 w-full"
                href="https://www.behance.net/matheuscarvalho121" target="_blank"
            >
                <span class="font-semibold">Portfolio</span>
            </a>
        </div>
        <div class="flex items-center justify-end w-full invisible xl:visible">
            <img src="/profile_picture.png" class="w-[400px] profile_picture rounded-full" />
        </div>
    </div>
    <div id="about" class="bg-[#010101] text-white pt-10 pb-20 xl:px-40">
        <h2 class="font-tech text-center text-3xl xl:text-5xl xl:pt-10">ABILITIES</h2>
        <div class="grid justify-center xl:grid-cols-3 mt-14">
            <CardsAbility title="Graphic Designer" description="Crafting Digital Experiences Creating seamless, user-centric websites for an intuitive online journey." />
            <CardsAbility title="Web Designer" description="Crafting Digital Experiences Creating seamless, user-centric websites for an intuitive online journey." />
            <CardsAbility title="Web Designer" description="Crafting Digital Experiences Creating seamless, user-centric websites for an intuitive online journey." />
        </div>
    </div>
    <div id="resume" class="bg-[#010101] text-white py-10 xl:px-40 pb-20">
        <h2 class="font-tech px-8 text-3xl pt-5 xl:text-5xl xl:pt-10 xl:mt-20">RESUME</h2>
        <div class="px-8 mt-5 lg:grid lg:grid-cols-2 lg:gap-x-5">
            <div class="bg-red-500 w-full lg:order-last h-72 lg:h-96">

            </div>
            <div class="max-h-96 overflow-scroll">
                <CustomsAccordion :resume_items="resume_items" />
            </div>
        </div>
    </div>
</main>
</template>

<style scoped>
.grey_gradient {
    background: rgb(0,0,0);
    background: linear-gradient(90deg, rgba(0,0,0,1) 0%, rgba(67,67,67,1) 100%); 
}

.profile_picture {
    box-shadow: -10px 10px 25px black;
}

</style>