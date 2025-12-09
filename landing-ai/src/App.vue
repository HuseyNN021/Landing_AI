<script setup>
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import FeaturesSection from './components/FeaturesSection.vue';
import containerImg from './assets/Images/ContainerImg.png'
import StatsSection from './components/StatsSection.vue';
import PricingSection from './components/PricingSection.vue';
import FaqSection from './components/FaqSection.vue';
import CTASection from './components/CTASection.vue';
import Footer from './components/Footer.vue';
import ScrollTest from './components/ScrollTest.vue';
</script>

<template>

    <section
    class="bg-cover bg-center bg-no-repeat"
    :style="{ backgroundImage: `url(${containerImg})` }"
  >
    <Navbar />
    <Hero />
  </section>
    <FeaturesSection/>
    <StatsSection/>
    <PricingSection/>
    <FaqSection/>
    <CTASection/>
    <Footer/>
    <!-- <ScrollTest/> -->
</template>

<style scoped>

</style>
