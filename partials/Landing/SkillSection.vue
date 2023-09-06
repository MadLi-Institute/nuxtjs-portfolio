<script setup>
const skill_data = [
    {
        title: "Eating",
        desc: "I love eating coz eating makes me happy",
        svg: "eating.png",
    },
    {
        title: "Playing",
        desc: "I love playing coz playing makes me happy",
        svg: "playing.png",
    },
    {
        title: "Sleeping",
        desc: "I love sleeping coz sleeping makes me happy",
        svg: "sleeping.png",
    },
];
</script>

<template>
    <div class="flex items-center justify-center">
        <div class="py-16 w-full">
            <div class="flex flex-col text-center items-center justify-center">
                <div>
                    <p
                        class="py-px px-3 mt-0 mx-0 mb-4 text-xs font-semibold text-white bg-pink-500 inline-block tracking-wider uppercase rounded-full"
                    >
                        Skills
                    </p>
                </div>
                <div
                    class="mt-0 mr-auto mb-6 ml-auto text-3xl font-bold leading-none text-gray-900 max-w-lg font-sans tracking-tight sm:text-4xl md:mx-auto"
                >
                    <p class="inline"></p>
                    <p
                        class="text-3xl font-bold leading-none text-gray-900 inline max-w-lg font-sans tracking-tight lg:text-5xl md:mx-auto"
                    >
                        Best of three skills
                    </p>
                </div>
            </div>
            <div class="container m-auto px-6 text-gray-500 md:px-12 xl:px-0">
                <div
                    class="mx-auto grid gap-6 md:w-3/4 lg:w-full lg:grid-cols-3"
                >
                    <div
                        v-for="(v, i) in skill_data"
                        :key="i"
                        class="bg-white text-center rounded-2xl shadow-xl px-8 py-12 sm:px-12 lg:px-8"
                    >
                        <div class="mb-12 space-y-4">
                            <h3 class="text-2xl font-semibold text-purple-900">
                                {{ v.title }}
                            </h3>
                            <p class="mb-6">
                                {{ v.desc }}
                            </p>
                            <NuxtLink
                                href="/about"
                                class="block font-medium text-purple-600"
                                >Know more</NuxtLink
                            >
                        </div>
                        <img
                            :src="`/media/landing/${v.svg}`"
                            class="w-auto h-32 mx-auto -mb-12"
                            :alt="v.svg"
                            loading="lazy"
                        />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>