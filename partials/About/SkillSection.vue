<script setup>
const skill_select = ref(1);
const raw_skill_one = [
  {
    id: 1,
    title: "Vue.js",
    src: "vuejs.svg",
    color: "emerald",
  },
  {
    id: 2,
    title: "Laravel",
    src: "laravel.svg",
    color: "red",
  },
  {
    id: 3,
    title: "Next.js",
    src: "nextjs.svg",
    color: "gray",
  },
];

const raw_skill_two = [
  {
    id: 4,
    title: "TailwindCSS",
    src: "tailwindcss.svg",
    color: "sky",
  },
  {
    id: 5,
    title: "MongoDB",
    src: "mongodb.svg",
    color: "green",
  },
  {
    id: 6,
    title: "Blender",
    src: "blender.svg",
    color: "orange",
  },
];

const raw_skill_desc = [
  {
    id: 1,
    title: "Vue.js",
    desc: "The Progressive Javascript Frameworks. An approachable, performant, and versatile framework for building web user interfaces.",
    sub: "Yeah totally nice",
  },
  {
    id: 2,
    title: "Laravel",
    desc: "Laravel is a web application framework with expressive, elegant syntax. We've already laid the foundation - freeing you to create without sweating the small things.",
    sub: "Yeah totally nice",
  },
  {
    id: 3,
    title: "Next.js",
    desc: "Used by some of the world's largest companies Next.js enables you to create full-stack Web applications by extending the latest React features, and intergrating powerful Rust-based JavaScript tooling for the fastest builds.",
    sub: "Yeah totally nice",
  },
  {
    id: 4,
    title: "TailwindCSS",
    desc: "A utility-first CSS framework packed with classes like flex, pt-4, text-center, and rotate-90 that can be composed to build any design, directly in your markup.",
    sub: "Yeah totally nice",
  },
  {
    id: 5,
    title: "MongoDB",
    desc: "MongoDB is a modern databse that supports transactional, search, analytics, and mobile use cases. It offers a flexible document data model, an unified query API, and cloud services for developers in any environment.",
    sub: "Yeah totally nice",
  },
  {
    id: 6,
    title: "Blender",
    desc: "Blender is a public project that offers a range of tools and features for modeling, sculpting, animation, VFX, and more.",
    sub: "Yeah totally nice",
  },
];
</script>

<template>
    <div class="py-16">
        <h3
            class="text-3xl text-gray-700 font-bold text-center tracking-widest md:text-5xl"
        >
            🎯SKILLS
        </h3>
        <div class="flex flex-wrap items-center">
            <div
                class="w-full md:w-6/12 px-4 mx-auto order-2 md:order-1 hidden md:block"
            >
                <div class="justify-center flex flex-wrap relative">
                    <div class="lg:my-4 w-full lg:w-6/12 px-4">
                        <SkillCard
                            @click="skill_select = v.id"
                            v-for="(v, i) in raw_skill_one"
                            :key="i"
                            :raw_data="v"
                        />
                    </div>
                    <div
                        class="lg:my-4 w-full lg:w-6/12 px-4 lg:mt-16 max-lg:[&>*:first-child]:mt-0"
                    >
                        <SkillCard
                            @click="skill_select = v.id"
                            v-for="(v, i) in raw_skill_two"
                            :key="i"
                            :raw_data="v"
                        />
                    </div>
                </div>
            </div>
            <div
                class="w-full md:w-4/12 px-12 md:px-4 mx-auto order-1 mt-16 h-fit md:order-2"
            >
                <template v-for="(v, i) in raw_skill_desc">
                    <SkillDesc
                        v-if="skill_select === v.id"
                        :raw_data="v"
                        :key="i"
                    />
                </template>
                <div class="block pb-6 md:hidden">
                    <SkillMiniBtn
                        @click="skill_select = v.id"
                        v-for="(v, i) in raw_skill_one"
                        :key="i"
                        :title="v.title"
                        :color="v.color"
                    />
                    <SkillMiniBtn
                        @click="skill_select = v.id"
                        v-for="(v, i) in raw_skill_two"
                        :key="i"
                        :title="v.title"
                        :color="v.color"
                    />
                </div>
            </div>
        </div>
    </div>
</template>