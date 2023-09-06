<template>
    <div class="flex items-center justify-center">
        <div class="w-full">
            <div class="flex bg-white" style="height: 600px">
                <div
                    class="flex items-center text-center lg:text-left px-8 md:px-12 lg:w-1/2"
                >
                    <div>
                        <h2
                            class="text-3xl font-semibold text-gray-800 md:text-5xl xl:text-5xl lg:font-bold"
                        >
                            Welcome to Madison&apos;s Portfolio
                            <span class="text-indigo-600">Idea</span>
                        </h2>
                        <p class="mt-2 text-sm text-gray-500 md:text-base lg:text-lg">
                            Lorem ipsum dolor sit amet, consectetur adipisicing
                            elit. Blanditiis commodi cum cupiditate ducimus,
                            fugit harum id necessitatibus odio quam quasi,
                            quibusdam rem tempora voluptates. Cumque debitis
                            dignissimos id quam vel!
                        </p>
                        <div class="flex justify-center lg:justify-start mt-6">
                            <NuxtLink
                                class="px-4 py-3 bg-gray-900 text-gray-200 text-xs font-semibold rounded hover:bg-gray-800"
                                href="/about"
                                >Learn More</NuxtLink
                            >
                        </div>
                    </div>
                </div>
                <div
                    class="hidden lg:block lg:w-1/2"
                    style="
                        clip-path: polygon(10% 0, 100% 0%, 100% 100%, 0 100%);
                    "
                >
                    <div
                        class="h-full object-cover"
                        style="background-image: url(/media/landing/welcome.jpg)"
                    >
                        <div class="h-full bg-black opacity-25"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>