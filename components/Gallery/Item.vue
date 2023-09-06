<script setup>
defineProps({
    raw_data: Object
})
</script>

<template>
    <div class="lg:w-1/3 sm:w-1/2 p-4">
        <div class="flex relative">
          <img alt="gallery" class="absolute inset-0 w-full h-full object-cover object-center rounded-xl" :src="`/media/gallery/${raw_data.image}`" :alt="raw_data.image">
          <div class="px-8 py-10 relative z-10 w-full border-4 border-gray-200 bg-white rounded-xl transition duration-200 ease-out transform opacity-0 hover:opacity-100">
            <h2 class="tracking-widest text-sm title-font font-medium text-indigo-500 mb-1">{{ raw_data.sub }}</h2>
            <h1 class="title-font text-lg font-medium text-gray-900 mb-3">{{ raw_data.title }}</h1>
            <p class="leading-relaxed">{{ raw_data.desc }}</p>
          </div>
        </div>
      </div>
</template>
