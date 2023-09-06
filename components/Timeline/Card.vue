<script setup>
defineProps({
    raw_data: Object
})
</script>

<template>
    <li class="border-l-2 border-green-600">
        <div class="md:flex flex-start ">
            <div
                class="bg-green-600 w-6 h-6 flex items-center justify-center rounded-full -ml-3.5"
            >
                <svg
                    aria-hidden="true"
                    focusable="false"
                    data-prefix="fas"
                    class="text-white w-3 h-3"
                    role="img"
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 448 512"
                >
                    <path
                        fill="currentColor"
                        d="M0 464c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48V192H0v272zm64-192c0-8.8 7.2-16 16-16h288c8.8 0 16 7.2 16 16v64c0 8.8-7.2 16-16 16H80c-8.8 0-16-7.2-16-16v-64zM400 64h-48V16c0-8.8-7.2-16-16-16h-32c-8.8 0-16 7.2-16 16v48H160V16c0-8.8-7.2-16-16-16h-32c-8.8 0-16 7.2-16 16v48H48C21.5 64 0 85.5 0 112v48h448v-48c0-26.5-21.5-48-48-48z"
                    ></path>
                </svg>
            </div>
            <div
                class="p-6 rounded-lg shadow-lg bg-gray-100 max-w-md ml-0 mb-10 w-full sm:ml-6"
            >
                <div class="flex justify-between mb-4">
                    <p
                        class="font-medium text-purple-600 hover:text-purple-700 focus:text-purple-800 duration-300 transition ease-in-out text-sm"
                        >{{ raw_data.title }}</p
                    >
                    <p v-if="raw_data.year_start && raw_data.year_end !== null"
                        class="font-medium text-purple-600 hover:text-purple-700 focus:text-purple-800 duration-300 transition ease-in-out text-sm"
                        >{{raw_data.year_start}} - {{raw_data.year_end}}</p
                    >
                </div>
                <p class="text-gray-700 mb-6">
                    {{ raw_data.desc }}
                </p>
                <ul class="list-disc text-gray-700 mb-6">
                    <li v-for="(v, i) in raw_data.desc_list" :key="i" class="list-inside">{{v}}</li>
                    <div v-if="raw_data.spec_list" class="ms-5">
                        <p class="ms-2 mt-1 mb-2">To be more specific, consider the following: </p>
                    <ul class="list-disc text-gray-700 mb-6 ms-5">
                        <li v-for="(v, i) in raw_data.spec_list" :key="i" class="list-none">{{ v }}</li>
                    </ul>
                    </div>
                </ul>
            </div>
        </div>
    </li>
</template>
