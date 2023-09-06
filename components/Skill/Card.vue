<script setup>
defineProps({
    raw_data: Object
})
</script>

<template>
    <div class="cursor-pointer transition duration-150 ease-out transform hover:scale-110 my-4 lg:my-8">
        <div :class="`bg-rose-300 shadow-lg rounded-lg text-center p-8 h-40`">
            <img
                alt="..."
                class="shadow-md rounded-lg max-w-full w-16 h-14 mx-auto p-2 bg-white"
                :src="`/media/about/skill-logos/${raw_data.src}`"
            />
            <p class="text-lg text-slate-900 mt-4 font-semibold">{{ raw_data.title }}</p>
        </div>
    </div>
</template>
