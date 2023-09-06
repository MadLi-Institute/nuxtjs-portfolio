<script setup>
defineProps({
    raw_data: Object
});
</script>

<template>
        <div
            class="p-3 text-center inline-flex items-center justify-center w-16 h-16 mb-6 shadow-lg rounded-full bg-slate-400"
        >
        🎑
        </div>
        <h3 class="text-3xl mb-2 font-bold leading-normal">
            {{ raw_data.title }}
        </h3>
        <p
            class="text-lg text-justify font-semibold leading-relaxed mt-4 mb-4"
        >
        {{ raw_data.desc }}
        </p>
        <p
            class="text-lg font-light leading-relaxed mt-4 mb-4"
        >
        {{ raw_data.sub }}
        </p>
</template>
