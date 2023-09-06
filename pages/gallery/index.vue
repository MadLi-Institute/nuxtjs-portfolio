<script setup lang="ts">
useSeoMeta({
    title: "Gallery - It's fun to share enjoyable stories with others"
})
const gallery_data = [
    {
        sub: "Web Development",
        title: "My First Ever Portfolio Website",
        desc: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Molestias officiis recusandae voluptate, adipisci iure minima aliquam illo accusamus sapiente perspiciatis quod qui earum nam nihil dicta, quisquam, aperiam autem consequatur!",
        image: "my-first-ever-portfolio.png"
    },
    {
        sub: "3D Modelling",
        title: "Gray Environment",
        desc: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Molestias officiis recusandae voluptate, adipisci iure minima aliquam illo accusamus sapiente perspiciatis quod qui earum nam nihil dicta, quisquam, aperiam autem consequatur!",
        image: "gray-env.png"
    },
    {
        sub: "DOTA 2",
        title: "My Favorite Support",
        desc: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Molestias officiis recusandae voluptate, adipisci iure minima aliquam illo accusamus sapiente perspiciatis quod qui earum nam nihil dicta, quisquam, aperiam autem consequatur!",
        image: "magnus-cypher.png"
    },
    {
        sub: "CSGO",
        title: "My Childhood FPS Game",
        desc: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Molestias officiis recusandae voluptate, adipisci iure minima aliquam illo accusamus sapiente perspiciatis quod qui earum nam nihil dicta, quisquam, aperiam autem consequatur!",
        image: "csgo-test.png"
    },
    {
        sub: "3D Modelling",
        title: "My First 3D Model",
        desc: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Molestias officiis recusandae voluptate, adipisci iure minima aliquam illo accusamus sapiente perspiciatis quod qui earum nam nihil dicta, quisquam, aperiam autem consequatur!",
        image: "my-ever-first-3d-model.png"
    },
    {
        sub: "Lol of Legend: Wildrift",
        title: "ana IO Support to Carry",
        desc: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Molestias officiis recusandae voluptate, adipisci iure minima aliquam illo accusamus sapiente perspiciatis quod qui earum nam nihil dicta, quisquam, aperiam autem consequatur!",
        image: "wildrift-io.jpg"
    },
]
</script>

<template>
    
    <Navbar />
    <section class="text-gray-600 body-font">
        <div class="container px-5 py-24 mx-auto">
          <div class="flex flex-col text-center w-full mb-20">
            <h1 class="sm:text-3xl text-2xl font-medium title-font mb-4 text-gray-900">It&apos;s fun to share enjoyable stories with others.</h1>
            <p class="lg:w-2/3 mx-auto leading-relaxed text-base">Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt laborum expedita reiciendis obcaecati recusandae. Cupiditate id aliquam autem dignissimos beatae, ipsam eum delectus facere vel repellat! Voluptatum beatae laboriosam accusantium.</p>
          </div>
          <div class="flex flex-wrap -m-4">
            <GalleryItem v-for="(v, i) in gallery_data" :key="i" :raw_data="v"/>
          </div>
        </div>
      </section>
</template>