<script setup>
import { onMounted } from 'vue';
import { gsap } from 'gsap';

onMounted(()=>{
    gsap.from('.statusContent>div',{
        duration: 0.9,
    scale: 0.8,
    opacity: 0,
    y: 20,
    stagger: 0.18,
    ease: 'power3.out'
    })
})
</script>

<template>
    <section class="w-full  mt-4">
        <hr class="text-white">
        <div class="statusContent flex justify-around">
            <div>
                <h3 class="text-[#FF541F] text-[0.5rem] md:text-[0.7rem] lg:text-[1.5rem]">clients</h3>
                <p class="font-bold text-white text-[1rem] md:text-[2rem] lg:text-[3rem]">120K+</p>
            </div>
            <div>
                <h3 class="text-[#FF541F] text-[0.5rem] md:text-[0.7rem] lg:text-[1.5rem]">Projects</h3>
                <p class="font-bold text-white text-[1rem] md:text-[2rem] lg:text-[3rem]">150+</p>
            </div>
            <div>
                <h3 class="text-[#FF541F] text-[0.5rem] md:text-[0.7rem] lg:text-[1.5rem]">5-Stars Review</h3>
                <p class="font-bold text-white text-[1rem] md:text-[2rem] lg:text-[3rem]">32K+</p>
            </div>
        </div>
        <hr class="text-white">
    </section>
</template>