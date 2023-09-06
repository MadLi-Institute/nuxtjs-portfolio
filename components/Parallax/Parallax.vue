<script setup>
defineProps({
    image: String
})
</script>

<template>
    <section
    class="flex flex-col w-full h-[300px] lg:h-[400px] xl:h-[500px] bg-cover bg-fixed bg-center justify-center items-center"
    :style="`background-image: url(/media/parallax-images/${image})`"
>
    <h1 class="text-white text-3xl font-bold lg:text-7xl lg:font-extralight mt-20">
        This is Parallax Effect
    </h1>

    <span class="text-center text-base lg:text-lg font-semibold my-20 text-white/90">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta maxime quo facere hic voluptates amet nostrum! Tenetur, recusandae ea. Vero iusto, vitae maiores quam ratione repudiandae nemo repellendus nobis accusamus!
    </span>
</section>
</template>