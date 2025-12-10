<script setup>
import containerImg from '../assets/Images/ContainerImg.png'
import { onMounted } from 'vue'
import { gsap } from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'
import ScrollTest from './ScrollTest.vue'
gsap.registerPlugin(ScrollTrigger)

onMounted(()=>{
 

  gsap.from("#pricingId", {
    scrollTrigger:{
        trigger: '#pricingId',
        start: "top 85%",
        toggleActions: 'play none none none'

    },
    duration: 1,
    y: -100,
    autoAlpha: 0,
    stagger: 0.05,
    ease: "power3.out"
  });
  gsap.from(".pricingContent", {
    scrollTrigger:{
        trigger: '.pricingContent',
        start: "top 85%",
        toggleActions: 'play none none none'

    },
    duration: 1,
    y: 100,
    autoAlpha: 0,
    stagger: 0.05,
    ease: "power3.out"
  });
})
</script>

<template>
    <section id="pricingNav" class="bg-cover bg-center bg-no-repeat pl-3"
    :style="{ backgroundImage: `url(${containerImg})` }">
        <div class="flex flex-col justify-center items-center gap-5">
            <div class="flex flex-col justify-center items-center">
                <h2 id="pricingId" class=" font-bold text-[2rem] md:text-[2.5rem] lg:text-[4rem] text-white w-[20rem] md:w-[29rem] lg:w-[37.5rem]">
                    Choose the Plan That’s Right for You
                </h2>
                <p  class="pricingContent text-[0.7rem] md:text-[1rem] lg:text-[1.25rem] text-[#D9D9D9] w-[23rem] md:w-[37rem] lg:w-[48rem]">
                    Giving you access to essential features and over 1,000 creative tools. 
                    Upgrade to the Pro Plan to unlock powerful AI capabilities, cloud syncing, 
                    and a whole new level of creative freedom.
                </p>
                <div class="pricingContent text-[0.7rem] lg:text-[1rem] bg-gray-900 rounded-2xl text-white flex items-center mt-1 px-3 py-1 gap-1">
                    <div class="bg-gray-700 rounded-xl px-2 py-1">Monthly</div>
                    <div>Yearly</div>
                </div>
            </div>
     
            
        </div>
        <ScrollTest/>
    </section>
    
</template>