<script setup>
</script>

<template>
    <div class="container mx-auto py-16">
        <div class="flex flex-col text-center justify-center mb-6">
            <div>
                <p
                    class="py-px px-3 mt-0 mx-0 text-xs font-semibold text-white bg-pink-500 inline-block tracking-wider uppercase rounded-full"
                >
                    Blog
                </p>
            </div>
            <div
                class="mt-0 mr-auto mb-6 ml-auto text-3xl font-bold leading-none text-gray-900 max-w-lg font-sans tracking-tight sm:text-4xl md:mx-auto"
            >
                <div class="inline-block relative">
                    <p
                        class="text-3xl font-bold leading-none text-gray-900 relative inline max-w-lg font-sans tracking-tight lg:text-5xl md:mx-auto"
                    >
                        Beat the heat
                    </p>
                </div>
            </div>
        </div>
        <div class="flex flex-col lg:flex-row justify-center items-stretch mx-4">
          <div class="lg:w-4/12 flex justify-center items-center text-center">
            <div class="lg:text-end lg:me-10">
              <h1 class="text-4xl md:text-5xl xl:text-6xl font-semibold">Life Diary</h1>
              <p class="text-base leading-normal lg:text-2xl ">The greatest joys is to create good memories.</p>
            </div>
          </div>
          <div class="lg:w-8/12 mt-6 md:mt-8 lg:mt-0">
            <div class="relative w-full h-full">
              <img src="/media/blog/main-picture.jpg" alt="sims-4" role="img" class="w-full h-full relative hidden lg:block rounded-lg" />
              <img src="/media/blog/main-picture.jpg" alt="sims-4" role="img" class="w-full h-full lg:hidden rounded-lg" />
              <div class="hidden lg:block absolute bottom-0 right-0 w-1/2">
                <NuxtLink href="/blog" class="text-xl xl:text-2xl font-medium flex justify-between w-full items-center p-5 xl:p-6 bg-pink-400 text-white">
                  Discover More
                  <div>
                    <svg class="fill-stroke" width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
                      <path d="M6.66663 16H25.3333" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                      <path d="M20 21.3333L25.3333 16" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                      <path d="M20 10.667L25.3333 16.0003" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                    </svg>
                  </div>
                </NuxtLink>
              </div>
            </div>
            <div class="mt-6 md:mt-8 lg:hidden">
              <NuxtLink href="/blog" class="text-base md:text-xl font-semibold leading-tight flex justify-between items-center px-5 py-4 lg:py-7 lg:px-7 w-full md:w-5/12 bg-pink-400 text-white">
                Discover More
                <div>
                  <svg class="fill-stroke" width="22" height="24" viewBox="0 0 22 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <g clip-path="url(#clip0)">
                      <path d="M0.453735 12H14.4537" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                      <path d="M10.4539 16L14.4539 12" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                      <path d="M10.4539 8L14.4539 12" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                    </g>
                    <defs>
                      <clipPath id="clip0">
                        <rect width="21.7269" height="24" fill="white" />
                      </clipPath>
                    </defs>
                  </svg>
                </div>
              </NuxtLink>
            </div>
          </div>
        </div>
      </div>
</template>