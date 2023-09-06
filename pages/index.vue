<script setup lang="ts">
import LandingSection from "@/partials/Landing/LandingSection.vue";
import SkillSection from "@/partials/Landing/SkillSection.vue";
import QuoteSection from "@/partials/Landing/QuoteSection.vue";
import BlogSection from "@/partials/Landing/BlogSection.vue";
import ContactSection from "@/partials/Landing/ContactSection.vue";

useSeoMeta({
    title: "Welcome to Madison's Portfolio",
    description: "Abnormal ang nag himo ani!!",
    ogDescription: "Still about Madison's Portfolio",
    ogTitle: "Welcome to Madison's Portfolio",
    ogImage: "about.jpg",
    twitterCard: "summary_large_image"
})
</script>

<template>
    
    <Navbar />
    <LandingSection />
    <Parallax image="parallax_doll_1.jpg"/>
    <SkillSection />
    <Parallax image="parallax_doll_2.jpg"/>
    <QuoteSection />
    <Parallax image="parallax_doll_3.jpg"/>
    <BlogSection />
    <Parallax image="parallax_doll_4.jpg"/>
    <ContactSection />
    <Footer />
</template>