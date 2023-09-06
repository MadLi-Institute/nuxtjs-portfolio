<script setup lang="ts">
import IntroSection from "@/partials/Blog/IntroSection.vue";

useSeoMeta({
    title: "Blog - Unleash creativity with a Personal Blog"
})
const blog_data = [
    {
        title: "Architecture: Modern House",
        tag: "Passion",
        desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur dolor, dolores totam nisi enim cum dicta nemo doloremque suscipit quod, soluta incidunt distinctio. Labore unde impedit commodi cupiditate, iure placeat?",
        image: "architecturedrawing.jpg",
        author: "ME",
        date_published: "August 31, 2023"
    },
    {
        title: "Architecture: Interior Design",
        tag: "Passion",
        desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur dolor, dolores totam nisi enim cum dicta nemo doloremque suscipit quod, soluta incidunt distinctio. Labore unde impedit commodi cupiditate, iure placeat?",
        image: "vivamagenta.png",
        author: "ME",
        date_published: "August 31, 2023"
    },
    {
        title: "Starry Night",
        tag: "Hobby",
        desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur dolor, dolores totam nisi enim cum dicta nemo doloremque suscipit quod, soluta incidunt distinctio. Labore unde impedit commodi cupiditate, iure placeat?",
        image: "nightsky.png",
        author: "ME",
        date_published: "August 31, 2023"
    },
    {
        title: "Postcard from Portugal",
        tag: "Interest",
        desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur dolor, dolores totam nisi enim cum dicta nemo doloremque suscipit quod, soluta incidunt distinctio. Labore unde impedit commodi cupiditate, iure placeat?",
        image: "portogalpostcard.jpg",
        author: "ME",
        date_published: "August 31, 2023"
    },
    {
        title: "Christmas Break Swimming",
        tag: "Vacation",
        desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur dolor, dolores totam nisi enim cum dicta nemo doloremque suscipit quod, soluta incidunt distinctio. Labore unde impedit commodi cupiditate, iure placeat?",
        image: "vacation.jpg",
        author: "ME",
        date_published: "August 31, 2023"
    },
    {
        title: "Heaven's Peak",
        tag: "Vacation",
        desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur dolor, dolores totam nisi enim cum dicta nemo doloremque suscipit quod, soluta incidunt distinctio. Labore unde impedit commodi cupiditate, iure placeat?",
        image: "heavenspeak.jpg",
        author: "ME",
        date_published: "August 31, 2023"
    },
]

</script>

<template>
    
    <Navbar />
    <IntroSection />

    <div class="flex items-center justify-center">
        <div class="text-gray-900 py-14 px-0 bg-white">
            <div
                class="w-full py-4 px-5 my-0 mx-auto space-y-5 sm:py-8 md:py-12 sm:space-y-8 md:space-y-16 max-w-7xl"
            >
                <div class="grid grid-cols-12 sm:px-5 gap-5">
                    <BlogItem v-for="(v, i) in blog_data" :key="i" :raw_data="v" :raw_id="i+1" />
                </div>
            </div>
        </div>
    </div>
</template>