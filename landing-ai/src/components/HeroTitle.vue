<script setup>
import { gsap } from "gsap";
import Button from '@/Reuseable/Button.vue';
import { onMounted } from "vue";


onMounted(() => {
 

  gsap.from("#heroId", {
    duration: 1,
    y: -100,
    autoAlpha: 0,
    stagger: 0.05,
    ease: "power3.out"
  });
});
</script>


<template>

    <section  id="heroId" class="w-full flex flex-col justify-center items-center gap-4">
        <h1 class=" font-modern font-bold leading-[2rem] md:leading-[4rem] lg:leading-[5rem] text-[1.5rem] md:text-[3.5rem] lg:text-[5rem]  text-center text-white w-[20rem] md:w-[45rem] lg:w-[62.5rem] ">
            Automate <span class="text-[#FF541F]">Intelligence</span>. Accelerate Growth.
        </h1>
        <p class="text-[#FFFFFFB2] text-[0.7rem] lg:text-[1.375rems] w-[20rem] md:w-[30rem] lg:w-[30rem] h-[5rem] text-center">
            Our AI-powered SaaS platform empowers
             businesses to streamline operations,
             automate repetitive tasks, and make smarter,
              data-driven decisions—all from one intuitive 
              dashboard.
        </p>
        <div class="flex gap-3">
            <Button :text="'Get Started'"/>
            <Button class="bg-black border border-[#FCFCFC3B]" :text="'See Details'"/>
        </div>
    </section>
</template>