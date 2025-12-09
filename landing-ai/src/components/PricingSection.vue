<script setup>
import containerImg from '../assets/Images/ContainerImg.png'
import { onMounted } from 'vue'
import { gsap } from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'
import PricingCard from './PricingCard.vue'
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
    <section id="pricingNav" class="bg-cover bg-center bg-no-repeat"
    :style="{ backgroundImage: `url(${containerImg})` }">
        <div class="flex flex-col justify-center items-center gap-5">
            <div class="flex flex-col justify-center items-center">
                <h2 id="pricingId" class=" font-bold text-[2rem] md:text-[2.5rem] lg:text-[4rem] text-white w-[20rem] md:w-[29rem] lg:w-[37.5rem]">
                    Choose the Plan That’s Right for You
                </h2>
                <p  class="pricingContent text-[0.7rem] md:text-[1rem] lg:text-[1.25rem] text-[#D9D9D9] w-[25rem] md:w-[37rem] lg:w-[48rem]">
                    Giving you access to essential features and over 1,000 creative tools. 
                    Upgrade to the Pro Plan to unlock powerful AI capabilities, cloud syncing, 
                    and a whole new level of creative freedom.
                </p>
                <div class="pricingContent bg-gray-900 rounded-2xl text-white flex items-center px-3 py-1 gap-1">
                    <div class="bg-gray-700 rounded-xl px-2 py-1">Monthly</div>
                    <div>Yearly</div>
                </div>
            </div>
            <!-- <div 
            class="
                flex overflow-x-auto snap-x snap-mandatory gap-4 px-4
                md:grid md:grid-cols-3 md:gap-6 md:overflow-visible
                items-center
                ">
                <div
                class="
                    min-w-[100%] snap-center
                    ml-15
                    h-[22rem]
                    lg:h-[30rem]
                    bg-[#272829B2]
                    p-4 rounded-xl
                    text-white
                    md:min-w-0 md:w-auto
                    flex flex-col
                    items-center
                "
                >
                <div class="flex flex-col gap-4">
                    <p class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">Pro</p>
                    <p class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">
                        Everything you need to supercharge your productivity.
                    </p>
                    <p><span class="text-[2.5rem]">$17</span> / month</p>
                </div> 
                <hr />
                <div class="flex flex-col gap-4 mt-3">
                    <p class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">What's included</p>
                    <ul class="flex flex-col gap-1">
                        <li class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">20 design generations/month</li>
                        <li class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">Low-res downloads</li>
                        <li class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">Basic style presets</li>
                        <li class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">Limited customization options</li>
                    </ul>
                </div>  
                <button
                    class="md:w-[10rem] lg:w-[10rem] px-6 py-2 rounded-xl border border-[#FF541F]/40
                                    bg-transparent text-white font-medium flex items-center gap-2
                                    shadow-[0_0_25px_rgba(255,84,31,0.35)]
                                    hover:shadow-[0_0_35px_rgba(255,84,31,0.55)]
                                    hover:bg-[#FF541F]
                                    transition-all duration-300 mt-auto"
                    >
                    Subscribe
                    <span class="text-xl">›</span>
                </button>            
                </div>
                <div
                class="
                    min-w-[100%] snap-center
                    h-[22rem]
                    lg:h-[35rem]
                    bg-[#272829B2]
                    p-4 rounded-xl
                    text-white
                    md:min-w-0 md:w-auto
                "
                >
                <div class="flex flex-col gap-4">
                    <p class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">Pro</p>
                    <p class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">
                        Everything you need to supercharge your productivity.
                    </p>
                    <p><span class="text-[2.5rem]">$17</span> / month</p>
                </div> 
                <hr />
                <div class="flex flex-col gap-4 mt-3">
                    <p class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">What's included</p>
                    <ul class="flex flex-col gap-1">
                        <li class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">20 design generations/month</li>
                        <li class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">Low-res downloads</li>
                        <li class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">Basic style presets</li>
                        <li class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">Limited customization options</li>
                    </ul>
                </div>  
                <button
                    class="md:w-[10rem] lg:w-[10rem] px-6 py-2 rounded-xl border border-[#FF541F]/40
                                    bg-transparent text-white font-medium flex items-center gap-2
                                    shadow-[0_0_25px_rgba(255,84,31,0.35)]
                                    hover:shadow-[0_0_35px_rgba(255,84,31,0.55)]
                                    hover:bg-[#FF541F]
                                    transition-all duration-300 mt-auto"
                    >
                    Subscribe
                    <span class="text-xl">›</span>
                </button>            
                </div>
                <div
                class="
                    min-w-[70%] snap-center
                    h-[22rem]
                    lg:h-[30rem]
                    bg-[#272829B2]
                    p-4 rounded-xl
                    text-white
                    md:min-w-0 md:w-auto
                "
                >
                <div class="flex flex-col gap-4">
                    <p class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">Pro</p>
                    <p class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">
                        Everything you need to supercharge your productivity.
                    </p>
                    <p><span class="text-[2.5rem]">$17</span> / month</p>
                </div> 
                <hr />
                <div class="flex flex-col gap-4 mt-3">
                    <p class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">What's included</p>
                    <ul class="flex flex-col gap-1">
                        <li class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">20 design generations/month</li>
                        <li class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">Low-res downloads</li>
                        <li class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">Basic style presets</li>
                        <li class="text-[0.7rem] md:text-[0.9rem] lg:text-[1rem]">Limited customization options</li>
                    </ul>
                </div>  
                <button
                    class="md:w-[10rem] lg:w-[10rem] px-6 py-2 rounded-xl border border-[#FF541F]/40
                                    bg-transparent text-white font-medium flex items-center gap-2
                                    shadow-[0_0_25px_rgba(255,84,31,0.35)]
                                    hover:shadow-[0_0_35px_rgba(255,84,31,0.55)]
                                    hover:bg-[#FF541F]
                                    transition-all duration-300 mt-auto"
                    >
                    Subscribe
                    <span class="text-xl">›</span>
                </button>            
                </div>
            </div> -->

          
            
        </div>
        <!-- <PricingCard class="mt-4"/> -->
         <ScrollTest/>
    </section>
    
</template>