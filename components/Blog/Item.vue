<script setup>
defineProps({
    raw_data: Object
})

const titleToSlug = (title) => {
    return title.toLowerCase().replace(/ /g,'-').replace(/[^\w-]+/g,'')
}
</script>

<template>
    <div
        class="flex flex-col items-start col-span-12 space-y-3 sm:col-span-6 xl:col-span-4 rounded-xl"
    >
        <NuxtLink
            :href="`blog/${titleToSlug(raw_data.title)}`"
            class="w-full mb-2 overflow-hidden rounded-lg shadow-sm max-h-56 relative"
        >
            <img :src="`/media/blog/${raw_data.image}`" class="object-cover transition duration-200 ease-out transform hover:scale-125" />
        </NuxtLink>
        <div class="px-2">
            <p
                class="bg-green-500 flex items-center leading-none text-sm font-medium text-gray-50 py-2 px-2 rounded-full w-fit"
            >
                {{ raw_data.tag }}
            </p>
        </div>
        <div class="px-2 h-36 overflow-auto">
            <h4 class="text-lg font-bold sm:text-xl md:text-2xl">
                {{ raw_data.title }}
            </h4>
            <p class="mt-2 text-sm text-black">
                {{ raw_data.desc }}
            </p>
        </div>
        <div class="py-2 px-2 self-end">
            <p class="inline text-xs font-medium mt-0 mr-1 underline"
                >{{ raw_data.author }}</p
            >
            <p class="inline text-xs font-medium mx-1">· {{ raw_data.date_published }}</p>
        </div>
    </div>
</template>
