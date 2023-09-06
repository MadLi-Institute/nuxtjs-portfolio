<script setup lang="ts">
import SelfSection from "@/partials/About/SelfSection.vue";
import TimelineSection from "@/partials/About/TimelineSection.vue";
import SkillSection from "@/partials/About/SkillSection.vue";
import CertSection from "@/partials/About/CertSection.vue";

useSeoMeta({
    title: "About - For Real"
})
</script>

<template>
    
    <Navbar />
    <SelfSection />
    <TimelineSection />
    <SkillSection />
    <CertSection />
    <Footer />
</template>