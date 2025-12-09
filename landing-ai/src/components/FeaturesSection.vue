<script setup>
import { onMounted } from 'vue'
import { gsap } from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

onMounted(()=>{
  gsap.from('.features',{
    scrollTrigger: {
      trigger: ".featuresGsap",
      start: "top 65%",
      toggleActions: "play none none none"
      // play = scroll-a çatanda animasiya et
      // none = başqa heç nə etmə
    },
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

    <section class="w-full  ">
        <div class="">
            <div class="flex items-center justify-center">
                <div class="text-white w-[20rem] md:w-[30rem] lg:w-[45rem]">
                    <h2 class="text-[2rem] md:text-[3rem] lg:text-[4rem]">
                        Designed for Designers. Powered by <span class="text-[#FF541F] font-bold">AI</span>.
                    </h2>
                    <p class="text-[1rem] font-normal text-[#FFFFFFD9]">
                        Unlock the full potential of your creativity with our AI-powered design assistant. 
                        Explore new dimensions of desig
                    </p>
                </div>
                <img class="w-[9.5rem] h-[9.5rem]" src="../assets/Images/rombusIcon.png" alt="">
            </div>
            <div class="p-4 featuresGsap">
                <!-- <div class="parent text-teal-50">
                    <div class="div1 flex p-4 rounded-[1.25rem]  bg-[linear-gradient(164deg,rgba(39,40,41,1)_0%,rgba(39,40,41,1)_62%,rgba(255,60,0,1)_100%)] ">
                        <div>
                            <p class="text-[0.7rem] lg:text-[1rem] text-[#D9D9D9D9]">
                                Skip the blank canvas and spark creativity instantly.
                                 Our AI generates high-quality, on-brand design concepts within seconds
                            </p>
                            <h4 class="text-[1.2rem] md:text-[1.7rem] lg:text-[2.125rem]">
                                Instant Ideation
                            </h4>
                        </div>
                        <div>
                            <img src="../assets/Images/Background.png" class="w-[4rem] " alt="">
                        </div>
                    </div>  
                    <div class="div2 p-4 flex rounded-[1.25rem]  bg-[#272829B2]"> 
                        <div>
                            <p class="text-[0.7rem] lg:text-[1rem] text-[#D9D9D9D9]">
                                No two creators are the same, and neither are their styles. 
                                Our AI learns from your inputs, understands your aesthetic preferences,
                                 and fine-tunes every design
                            </p>
                            <h4 class="text-[1.2rem] md:text-[1.7rem] lg:text-[2.125rem]">
                                Smart Adaptability
                            </h4>
                        </div>
                        <div>
                            <img src="../assets/Images/Background.png" class="w-[4rem]" alt="">
                        </div>
                    </div>
                    <div class="div3 px-4 py-6  flex rounded-[1.25rem]  bg-[#272829B2]"> 
                        <div>
                            <p class="text-[0.7rem] lg:text-[1rem] text-[#D9D9D9D9]">
                                Design once, export anywhere. 
                                Whether you need high-res graphics for print, 
                                responsive visuals for the web, mobile-optimized assets,
                            </p>
                            <h4 class="text-[1.2rem] md:text-[1.7rem] lg:text-[2.125rem]">
                                Multi-Format Export
                            </h4>
                        </div>
                        <div>
                            <img src="../assets/Images/Background.png" class="w-[4rem]" alt="">
                        </div>
                    </div>
                    <div class="div4 p-4 rounded-[1.25rem] flex   bg-[linear-gradient(164deg,rgba(39,40,41,1)_0%,rgba(39,40,41,1)_62%,rgba(255,60,0,1)_100%)] ">
                        <div>
                            <p class="text-[0.7rem] lg:text-[1rem] text-[#D9D9D9D9]">
                                Say goodbye to repetitive tweaks and endless back-and-forths. With intuitive prompt-based editing
                            </p>
                            <h4 class="text-[1.2rem] md:text-[1.7rem] lg:text-[2.125rem]">
                                Seamless Revisions
                            </h4>
                        </div>
                        <div>
                            <img src="../assets/Images/Background.png" class="w-[4rem]" alt="">
                        </div>
                    </div>
                </div> -->
                <div class="features grid grid-cols-1 md:grid-cols-5 gap-3 text-white">
    
                    <!-- BOX 1 -->
                    <div class="col-span-1 md:col-span-2 px-4 py-6 rounded-[1.25rem] 
                                bg-[linear-gradient(164deg,rgba(39,40,41,1)_0%,rgba(39,40,41,1)_62%,rgba(255,60,0,1)_100%)] flex">
                        <div class="flex-1">
                            <p class="text-[0.7rem] lg:text-[1rem] text-[#D9D9D9D9]">
                                Skip the blank canvas and spark creativity instantly.
                                Our AI generates high-quality, on-brand design concepts within seconds
                            </p>
                            <h4 class="text-[1.2rem] md:text-[1.7rem] lg:text-[2.125rem]">
                                Instant Ideation
                            </h4>
                        </div>
                        <img src="../assets/Images/Background.png" class="w-[4rem] h-[4rem]" />
                    </div>

                    <!-- BOX 2 -->
                    <div class="col-span-1 md:col-span-3 px-4 py-6 rounded-[1.25rem] bg-[#272829B2] flex">
                        <div class="flex-1">
                            <p class="text-[0.7rem] lg:text-[1rem] text-[#D9D9D9D9]">
                                No two creators are the same, and neither are their styles. 
                                Our AI learns from your inputs...
                            </p>
                            <h4 class="text-[1.2rem] md:text-[1.7rem] lg:text-[2.125rem]">
                                Smart Adaptability
                            </h4>
                        </div>
                        <img src="../assets/Images/Background.png" class="w-[4rem] h-[4rem]" />
                    </div>

                    <!-- BOX 3 -->
                    <div class="col-span-1 md:col-span-3 px-4 py-6 rounded-[1.25rem] bg-[#272829B2] flex">
                        <div class="flex-1">
                            <p class="text-[0.7rem] lg:text-[1rem] text-[#D9D9D9D9]">
                                Design once, export anywhere... 
                            </p>
                            <h4 class="text-[1.2rem] md:text-[1.7rem] lg:text-[2.125rem]">
                                Multi-Format Export
                            </h4>
                        </div>
                        <img src="../assets/Images/Background.png" class="w-[4rem] h-[4rem]" />
                    </div>

                    <!-- BOX 4 -->
                    <div class="col-span-1 md:col-span-2 p-4 rounded-[1.25rem] 
                                bg-[linear-gradient(164deg,rgba(39,40,41,1)_0%,rgba(39,40,41,1)_62%,rgba(255,60,0,1)_100%)] flex">
                        <div class="flex-1">
                            <p class="text-[0.7rem] lg:text-[1rem] text-[#D9D9D9D9]">
                                Say goodbye to repetitive tweaks and endless back-and-forths...
                            </p>
                            <h4 class="text-[1.2rem] md:text-[1.7rem] lg:text-[2.125rem]">
                                Seamless Revisions
                            </h4>
                        </div>
                        <img src="../assets/Images/Background.png" class="w-[4rem] h-[4rem]"/>
                    </div>

                </div>

            </div>
        </div>
    </section>
</template>

<style scoped>
    .parent {
display: grid;
grid-template-columns: repeat(5, 1fr);
grid-template-rows: repeat(5, 1fr);
grid-column-gap: 10px;
grid-row-gap: 10px;
}

.div1 { grid-area: 1 / 1 / 2 / 3; }
.div2 { grid-area: 1 / 3 / 2 / 6; }
.div3 { grid-area: 2 / 1 / 3 / 4; }
.div4 { grid-area: 2 / 4 / 3 / 6; }
</style>