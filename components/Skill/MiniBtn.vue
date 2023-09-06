<script setup>
defineProps({
    title: String,
    color: String
});
</script>

<template>
    <span
        :class="`text-xs font-semibold inline-block py-1 px-2 rounded-full bg-${color}-600 last:mr-0 mr-2 mt-2 cursor-pointer hover:scale-110 text-white`"
    >
        {{ title }}
    </span>
</template>
