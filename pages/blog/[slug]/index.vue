<script setup>
const route = useRoute();

const blog_data = [
    {
        title: "Architecture: Modern House",
        tag: "Passion",
        desc: "This is my first drawing on a single sheet of paper. This is large and difficult because I am drawing on a rough surfaced plywood. I mastered this talent as a high school student studying technical drafting. I prefer conducting technical drawing exercises at school since they have all of the necessary tools and the environment is pleasant and peaceful. My first course of study will be architecture, however there are no architectural programs in my city.",
        image: "architecturedrawing.jpg",
        author: "ME",
        date_published: "August 31, 2023"
    },
    {
        title: "Architecture: Interior Design",
        tag: "Passion",
        desc: "This is my current 3D model, as I would like to review and improve my 3D modeling skills. Despite being inexperienced and having only basic knowledge, I want to retain this skill. For the interior design, I utilized pre-made assets and incorporated the Viva Magenta analogous color scheme, which is the designated color of the year for 2023.",
        image: "vivamagenta.png",
        author: "ME",
        date_published: "August 31, 2023"
    },
    {
        title: "Starry Night",
        tag: "Hobby",
        desc: "It was a night shot with my smartphone. The power went out so I decided to take a picture of the sky. I set my mobile camera to manual mode, then set the exposure time to 30 seconds so I could take pictures of the stars. It's worth the wait even in the dark. I've done it before and I have a lot of photos and the best one I have is a view of the Milky Way.",
        image: "nightsky.png",
        author: "ME",
        date_published: "August 31, 2023"
    },
    {
        title: "Postcard from Portugal",
        tag: "Interest",
        desc: "This is the second postcard I received from Portugal after Lithuania. Exchanging postcards with people you meet online has been a great experience for me because it's something of value made by people you love and collect. It was confusing at first because it revealed your real address to them, but what I did was get to know them well and gain their trust first. Unfortunately, I am no longer in contact with them. I plan to do it again in the future and join the penpal community.",
        image: "portogalpostcard.jpg",
        author: "ME",
        date_published: "August 31, 2023"
    },
    {
        title: "Christmas Break Swimming",
        tag: "Vacation",
        desc: "Swimming here is a fun experience. During the Christmas holidays, it's time to relax and soak. I think it's best to stay home because my Christmas break is already planned for fully learning about Vue.js and Laravel web framework, but it wouldn't be good to spend time learning so as it is a chance to relax my mind and have some fun. It's time to experience.",
        image: "vacation.jpg",
        author: "ME",
        date_published: "August 31, 2023"
    },
    {
        title: "Heaven's Peak",
        tag: "Vacation",
        desc: "This is a site where you can observe a variety of blooms that are instagrammable and worth seeing, especially during the summer. This time it felt freezing because I was wearing a plain shirt and shorts and had not considered the temperature.",
        image: "heavenspeak.jpg",
        author: "ME",
        date_published: "August 31, 2023"
    },
]

const titleToSlug = (title) => {
    return title.toLowerCase().replace(/ /g,'-').replace(/[^\w-]+/g,'')
}
</script>

<template>
    <Navbar />
    <div class="flex items-center justify-center">
        <div class="mt-6 bg-gray-50">
            <div class="py-6 mx-auto">
                <template v-for="(v, i) in blog_data">
                    <BlogContent v-if="titleToSlug(v.title) === route.params.slug" :raw_data="v" :key="i"/>
                </template>
            </div>
        </div>
    </div>
</template>
