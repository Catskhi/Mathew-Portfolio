<script setup lang="ts">

const ui = /*ui*/ {
  background: 'bg-white dark:bg-slate-900'
}

</script>

<template>
<main>
    <LayoutNavbar />
    <div class="bg-[url('/Background_image.png')] h-screen w-screen bg-cover bg-center bg-no-repeat absolute" />
    <div class="h-screen w-creen grey_gradient"></div>
    <div class="lg:px-40 absolute top-0 w-screen flex">
        <div class="w-full h-screen text-white z-10 flex flex-col justify-center px-8 lg:w-1/3">
            <p class="font-inter text-xl lg:text-2xl font-semibold">Simpler as f***</p>
            <h1 class="text-[50px] lg:text-[60px] font-extrabold">
                MATHEUS
                <span class="mt-5">CARVALHO</span>
            </h1>
            <p class="mt-5 lg:text-lg">
                Simplicity is Elegance - Minimalist Design <br> by Matheus Carvalho
            </p>
            <button class="bg-[#E6E6E6] text-black font-inter mt-8 py-2 rounded text-left px-5 cursor-pointer hover:brightness-75 active:scale-[99%] transition-all duratio-300
            ">
                <span class="font-semibold">Portfolio</span>
            </button>
        </div>
        <div class="flex items-center justify-end w-full pr-40 hidden xl:visible">
            <img src="/profile_picture.png" class="w-[400px] profile_picture rounded-full" />
        </div>
    </div>
    <div id="about" class="bg-[#010101] text-white pt-10 pb-20 xl:px-40">
        <h2 class="font-tech text-center text-3xl xl:text-5xl xl:pt-10">ABILITIES</h2>
        <div class="flex px-10 mt-14 flex-col space-y-10 xl:flex-row">
            <CardsAbility class="xl:mt-12" title="Graphic Designer" description="Crafting Digital Experiences Creating seamless, user-centric websites for an intuitive online journey." />
            <CardsAbility title="Web Designer" description="Crafting Digital Experiences Creating seamless, user-centric websites for an intuitive online journey." />
            <CardsAbility title="Web Designer" description="Crafting Digital Experiences Creating seamless, user-centric websites for an intuitive online journey." />
        </div>
    </div>
    <div id="resume" class="bg-[#010101] text-white py-10 xl:px-40">
        <h2 class="font-tech px-8 text-3xl pt-5 xl:text-5xl xl:pt-10 xl:mt-20">RESUME</h2>
        <div class="px-8 mt-5">
            <div class="bg-red-500 w-full h-72">

            </div>
            <div class="mt-5 space-y-5">
                <BoxesExpansion title="test" />
                <BoxesExpansion title="test" />
                <BoxesExpansion title="test" />
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