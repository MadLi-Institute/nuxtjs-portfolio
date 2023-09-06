<script setup>
const education = "📚EDUCATION".split(/(?!$)/u);
const details = "🔍DETAILS".split(/(?!$)/u);

const education_data = [
    {
        title: "🏫 Southeast University",
        year_start: "2019",
        year_end: "2023",
        desc: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Fugit modi assumenda dignissimos odio facere explicabo tempore, fugiat aliquam, aspernatur officiis optio enim similique corrupti, debitis ab accusantium incidunt repellendus saepe?",
        desc_list: ["Bachelor of Science in Sleeping Management 💤🤵", "Best in Sleeping 😪", "Most Behave 🎀"]
    },
    {
        title: "🏢 Southern College",
        year_start: "2013",
        year_end: "2019",
        desc: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Fugit modi assumenda dignissimos odio facere explicabo tempore, fugiat aliquam, aspernatur officiis optio enim similique corrupti, debitis ab accusantium incidunt repellendus saepe?",
        desc_list: ["TVL - Sleeping Technology 💤👩‍💻", "Sleeping Systems Servicing NC-IV Holder 💤📄"]
    },
]

const details_data = [
    {
        title: "🎮 DOTA 2 Professional Scene",
        year_start: "2017",
        year_end: "2019",
        desc: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Fugit modi assumenda dignissimos odio facere explicabo tempore, fugiat aliquam, aspernatur officiis optio enim similique corrupti, debitis ab accusantium incidunt repellendus saepe?",
        desc_list: ["Best in Carry 🗡🐱‍👤", "Best in Midlane ⚡🐼", "Best in Offline 🪓😡", "Best in Soft Support ✊🐹", "Best in Hard Support 🍢🦁"]
    },
    {
        title: "🏓 Hobby & Interest",
        year_start: null,
        year_end: null,
        desc: "",
        desc_list: ["Eating 🍝", "Playing 🎮", "Sleeping 😴", "Ambot unsa pay lain interest sa ako life kay ako life walay interest sako 🤣", "Professional, Cleaver, & Chubby Cute Girl 👷‍♀️👩‍🔬"],
        spec_list: [
            "🏗🩺 Professional Engineer with Doctor of Engineering",
            "📐🩺 Professional Architect with Doctor of Architecture",
            "🛳⚓ Cruise Ship Captain with Doctor of Maritime Management",
            "✈🛩 Commercial Plane Captain with Doctor of Aviation",
            "🏫🎓 Professsor with Doctor of Education & Philosophy",
            "🔮🩺 Professional Psychologist with Doctor of Psychology"

        ]
    },
    {
        title: "🀄 Languages",
        year_start: null,
        year_end: null,
        desc: "",
        desc_list: ["Bisaya 🍍", "Tagalog 🌄", "English ⛰", "French 🎨"]
    }
]
</script>

<template>
    <div class="flex flex-col items-center justify-center py-16 xl:flex-row">
        <div class="flex flex-col items-center lg:flex-row">
            <div class="hidden flex-col px-5 items-center lg:flex">
                <h3 v-for="(v, i) in education" :key="i" class="text-5xl text-gray-700 font-bold py-1">{{ v }}</h3>
            </div>
            <div class="flex flex-col lg:hidden">
                <h3 class="text-3xl text-gray-700 font-bold py-1 tracking-widest md:text-5xl">📚EDUCATION</h3>
            </div>
            <ol class="group [&>li:first-child]:border-purple-600 [&>li:first-child>div>div:first-child]:bg-purple-600">
                <TimelineCard v-for="(v, i) in education_data" :key="i" :raw_data="v"/>
            </ol>
        </div>
        <div class="flex flex-col items-center lg:flex-row">
            <div class="hidden flex-col px-5 items-center lg:flex">
                <h3 v-for="(v, i) in details" :key="i" class="text-5xl text-gray-700 font-bold py-1">{{ v }}</h3>
            </div>
            <div class="flex flex-col lg:hidden">
                <h3 class="text-3xl text-gray-700 font-bold py-1 tracking-widest md:text-5xl">🔍DETAILS</h3>
            </div>
            <ol class="group [&>li:first-child]:border-purple-600 [&>li:first-child>div>div:first-child]:bg-purple-600">
                <TimelineCard v-for="(v, i) in details_data" :key="i" :raw_data="v"/>
            </ol>
        </div>
    </div>
</template>