<script setup>
import { onMounted } from 'vue'
import { gsap } from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'
import Button from '@/Reuseable/Button.vue';

gsap.registerPlugin(ScrollTrigger)

onMounted(() => {
  gsap.from(".statsContent > div", {
    scrollTrigger: {
      trigger: ".statsContent",
      start: "top 85%",
      toggleActions: "play none none none"
    },
    opacity: 0,
    y: 40,
    duration: 0.8,
    stagger: 0.2,
    ease: "power3.out"
  })
})
</script>

<template>
    <section class="w-full ">
        <div class="flex flex-col justify-center items-center gap-4">
            <div class="text-white flex flex-col md:flex-row lg:flex-row items-center justify-center">
                <p>2025</p>
                <p class="w-[20rem] md:w-[35rem] lg:w-[50rem] font-bold text-[0.7rem] md:text-[1rem] lg:text-[1.7rem] ">
                    Whether you're designing for personal projects, creative teams, or large-scale campaigns,
                     our AI-powered platform is built to bring your ideas to life—quickly, beautifully, and intelligently.
                     And the results? The numbers speak for themselves:
                </p>
            </div>
            <div class="statsContent grid grid-cols-2 lg:grid-cols-4 gap-10 place-items-center px-10">
                <div class="flex flex-col">
                    <div class="text-white">
                        <h3 class="text-[2rem] md:text-[2.5rem] lg:text-[4rem] font-bold">
                            2014
                        </h3>
                        <p class="text-[0.7rem] md:text-[1rem] lg:text-[1.375rem]">
                            Year of establishment
                        </p>
                        <p class="text-[#8F8E8E] text-[0.5rem] lg:text-[0.875rem]">
                            More than 10 years in the field
                        </p>
                    </div>
                    <div>
                        <img src="../assets/Images/images.png" class="w-[10rem] md:w-[14rem] lg:w-[18rem] h-[3rem] md:h-[4.5] lg:h-[5.7rem]" alt="">
                    </div>
                </div>
                <div class="flex flex-col mt-25">
                    <div class="text-white">
                        <h3 class="text-[2rem] md:text-[2.5rem] lg:text-[4rem] font-bold">
                            304
                        </h3>
                        <p class="text-[0.7rem] md:text-[1rem] lg:text-[1.375rem]">
                           Projects are launched
                        </p>
                        <p class="text-[#8F8E8E] text-[0.5rem] lg:text-[0.875rem]">
                            A lot of projects are done
                        </p>
                    </div>
                    <div>
                        <img src="../assets/Images/images (1).png" class="w-[10rem] md:w-[14rem] lg:w-[18rem] h-[3rem] md:h-[4.5] lg:h-[5.7rem]" alt="">
                    </div>
                </div>
                <div class="flex flex-col">
                    <div class="text-white">
                        <h3 class="text-[2rem] md:text-[2.5rem] lg:text-[4rem] font-bold">
                            189
                        </h3>
                        <p class="text-[0.7rem] md:text-[1rem] lg:text-[1.375rem]">
                            Clients are satisfied
                        </p>
                        <p class="text-[#8F8E8E] text-[0.5rem] lg:text-[0.875rem]">
                            These people love us
                        </p>
                    </div>
                    <div>
                        <img src="../assets/Images/images.png" class="w-[10rem] md:w-[14rem] lg:w-[18rem] h-[3rem] md:h-[4.5] lg:h-[5.7rem]" alt="">
                    </div>
                </div>
                <div class="flex flex-col lg:mt-25">
                    <div class="text-white">
                        <h3 class="text-[2rem] md:text-[2.5rem] lg:text-[4rem] font-bold">
                            12
                        </h3>
                        <p class="text-[0.7rem] md:text-[1rem] lg:text-[1.375rem]">
                            Projects in work
                        </p>
                        <p class="text-[#8F8E8E] text-[0.5rem] lg:text-[0.875rem]">
                            What we do right now
                        </p>
                    </div>
                    <div>
                        <img src="../assets/Images/images (1).png" class="w-[10rem] md:w-[14rem] lg:w-[18rem] h-[3rem] md:h-[4.5] lg:h-[5.7rem]" alt="">
                    </div>
                </div>
           </div>
          <div class="flex gap-4">
                <Button class="!w-[10rem]" :text="'Get Started →'"/>
                <Button class="bg-black border border-[#FCFCFC3B] !w-[10rem]" :text="'Slots are avaliable'"/>
          </div>
        </div>
    </section>
</template>