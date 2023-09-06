<script setup>
const self_data = {
    name: "Madison Li",
    sub: "You'd think being surrounded by cutting edge laboratory eqiupment and some of the greatest minds the world's ever known would be enough. Only problem is the lack of transparency. I don't think we get the full story on everything that occurs down here.",
    best_in: ["I can eat 🍽", "I can play 🎮", "I can breath 🌬"],
    image: "me.jpg",
};
</script>

<template>
    <div class="flex items-center justify-center">
        <section class="relative pt-12">
            <div class="items-center flex flex-wrap">
                <div class="w-full md:w-6/12 mx-auto px-4">
                    <img
                        :alt="self_data.image"
                        class="max-w-full rounded-xl shadow-lg"
                        :src="`/${self_data.image}`"
                    />
                </div>
                <div class="w-full md:w-5/12 mx-auto px-4">
                    <div class="md:pr-12">
                        <div
                            class="text-pink-600 p-3 text-center inline-flex items-center justify-center w-16 h-16 mb-6 shadow-lg rounded-full bg-pink-300 mt-8"
                        >
                            <i class="fas fa-rocket text-xl"></i>
                        </div>
                        <h3 class="text-3xl lg:text-7xl font-bold">
                            {{ self_data.name }}
                        </h3>
                        <p class="lg:mt-4 text-lg lg:text-3xl leading-relaxed">
                            {{ self_data.sub }}
                        </p>
                        <ul
                            class="list-none mt-6 text-base font-semibold lg:text-2xl"
                        >
                            <li v-for="(v, i) in self_data.best_in" :key="i" class="md:py-1">
                                <div class="flex items-center">
                                    <div>
                                        <span
                                            class="inline-block py-1 px-2 uppercase rounded-full text-pink-600 bg-pink-200 mr-3"
                                            ><i class="fas fa-fingerprint"></i
                                        ></span>
                                    </div>
                                    <div>
                                        <h4 class="">{{ v }}</h4>
                                    </div>
                                </div>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>