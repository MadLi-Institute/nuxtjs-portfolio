<script setup>
const achieve_data = [
    {
        title: "Latest Trends in Architecture Design 101: Shaping the future in Today's Architecture",
        date: "August",
        year: "2023",
        image: "architecture.png",
        issued_by: "MSTConnect",
    },
    {
        title: "Web Developer Webinar",
        date: "August",
        year: "2023",
        image: "web-dev-webinar.png",
        issued_by: "GoIT Philippines",
    },
    {
        title: "Machine Learning Fundamentals",
        date: "August",
        year: "2023",
        image: "machine-learning.png",
        issued_by: "Xaltius Academy",
    },
    {
        title: "Tools to use to Improve Performance in Azure SQL Database",
        date: "August",
        year: "2023",
        image: "azure.png",
        issued_by: "STYADA.DEV",
    },
    {
        title: "Igniting Innovation: The Ultimate Guide to Entrepreneurship",
        date: "August",
        year: "2023",
        image: "entrepreneur.png",
        issued_by: "UniAthena",
    },
    {
        title: "Integrating AI to Medical Coding: An Introduction for Aspiring Healthcare Professionals in the Field of Medical Coding",
        date: "September",
        year: "2023",
        image: "medical-coding.png",
        issued_by: "1Nurse",
    },
];
</script>

<template>
    <div class="py-16">
        <h3
            class="text-3xl text-gray-700 font-bold text-center tracking-widest md:text-5xl"
        >
            📜Certificates
        </h3>
        <div class="w-full mx-auto md:w-9/12">
            <div class="w-full text-gray-700 bg-gray-100 rounded-lg">
                <div class="flex flex-wrap flex-grow mt-5 h-96 overflow-x-hidden">
                    <div class="w-full px-4 my-1">
                        <div v-for="(v,i) in achieve_data" :key="i"
                            class="flex flex-col shadow-lg px-5 py-2 rounded-lg text-base lg:text-3xl transition duration-150 ease-out transform hover:scale-105"
                        >
                            <NuxtLink :href="`media/about/certificates/${v.image}`" target="_blank">
                                <h3 class="text-center py-3 font-semibold">
                                   {{ v.title }}
                                </h3>
                                <p>Date: {{ v.date}}, {{ v.year}}</p>
                                <h2>Issued by: <span class="font-semibold italic">{{ v.issued_by}}</span></h2>
                            </NuxtLink>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
