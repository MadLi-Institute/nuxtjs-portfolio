<script setup>
defineProps({
  raw_data: Object,
});
</script>

<template>
  <Head>
    <Title>{{ raw_data.title }}</Title>
  </Head>
  <Breadcrumb class="mt-5" :title="raw_data.title" />
  <div class="max-w-6xl px-5 py-6 mx-auto bg-gray-50">
    <img
      class="object-cover w-full shadow-sm h-full rounded-xl"
      :src="`../media/blog/${raw_data.image}`"
    />

    <div class="flex items-center justify-start my-4 px-1 md:px-8">
      <div
        class="px-2 py-1 font-bold bg-green-500 text-white rounded-lg hover:bg-green-400"
      >
        {{ raw_data.tag }}
      </div>
    </div>
    <div class="mt-2 px-1 md:px-8">
      <h3 class="text-3xl md:text-5xl font-bold text-gray-700">
        {{ raw_data.title }}
      </h3>

      <div class="flex justify-start items-center mt-2">
        <p
          class="text-sm text-green-500 font-bold bg-gray-100 rounded-full py-2 px-2 hover:text-red-500"
        >
          3000
        </p>
        <p class="text-sm text-gray-400 font-bold ml-5">Views</p>
      </div>

      <div class="font-light text-gray-600 flex items-center my-6">
        <img
          :src="`../about.jpg`"
          alt="avatar"
          class="hidden object-cover w-14 h-14 mx-4 rounded-full sm:block"
        />
        <h1 class="font-bold text-gray-700 hover:underline">
          By {{ raw_data.author }}
        </h1>
      </div>
    </div>

    <div
      class="max-w-4xl mx-auto text-2xl text-gray-700 mt-4 rounded bg-gray-100"
    >
      <div>
        <p class="mt-2 p-4 md:p-8">
          {{ raw_data.desc }}
        </p>
      </div>
    </div>
  </div>
  <Breadcrumb class="mt-5" :title="raw_data.title" />
</template>
