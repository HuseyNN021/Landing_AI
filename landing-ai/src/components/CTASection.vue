<script setup>
import Button from '@/Reuseable/Button.vue';
import { onMounted } from 'vue'
import { gsap } from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)
onMounted(()=>{
    gsap.from('#ctaId',{
    scrollTrigger: {
      trigger: "#ctaId",
      start: "top 85%",
      toggleActions: "play none none none"
      // play = scroll-a çatanda animasiya et
      // none = başqa heç nə etmə
    },
    duration: 0.9,
    scale: 0.8,
    opacity: 0,
    x: 20,
    stagger: 0.18,
    ease: 'power3.out'
  })
})
</script>

<template>
    <section id="ctaNav" class="w-full p-1">
       <div
            class="flex justify-center items-center h-[70vh]
     bg-[linear-gradient(183deg,rgba(0,0,0,1)_0%,rgba(39,40,41,1)_65%,rgba(255,60,0,1)_100%)]            "
        >
            <div id="ctaId" class="flex flex-col justify-center items-center gap-3 border  bg-[radial-gradient(50%_60%_at_50%_32.8%,rgba(255,255,255,0.4)_7.35%,rgba(255,84,31,0.32)_24.23%,rgba(247,175,153,0.4)_36%,rgba(255,84,31,0.4)_49.99%,rgba(0,0,0,0)_100%)]
            bg-black overflow-x-hidden border border-amber-50 p-7 rounded-2xl">
                <h2 class="font-bold text-[2rem] md:text-[2.5rem] lg:text-[4rem] text-white w-[20rem] md:w-[29rem] lg:w-[50rem]">
                    Ready to Design Smarter?
                </h2>
                <p class="text-[0.7rem] md:text-[1rem] lg:text-[1.25rem] text-[#D9D9D9] w-[24rem] md:w-[37rem] lg:w-[48rem] pl-3">
                    Whether you're a freelancer, a team, or a growing agency—our tools adapt to your workflow. Design faster. Deliver better.       
                </p>
                <Button :text="'Get Started →'"/>
            </div>
        </div>
    </section>
</template>