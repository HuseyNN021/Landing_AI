<script setup>
import containerImg from '../assets/Images/ContainerImg.png'

</script>

<template>
    <section class="bg-cover bg-center bg-no-repeat"
    :style="{ backgroundImage: `url(${containerImg})` }">
        <div class="flex flex-col justify-center items-center gap-5">
            <div class="flex flex-col justify-center items-center">
                <h2 class="font-bold text-[2rem] md:text-[2.5rem] lg:text-[4rem] text-white w-[20rem] md:w-[29rem] lg:w-[37.5rem]">
                    Choose the Plan That’s Right for You
                </h2>
                <p class="text-[0.7rem] md:text-[1rem] lg:text-[1.25rem] text-[#D9D9D9] w-[25rem] md:w-[37rem] lg:w-[48rem]">
                    Giving you access to essential features and over 1,000 creative tools. 
                    Upgrade to the Pro Plan to unlock powerful AI capabilities, cloud syncing, 
                    and a whole new level of creative freedom.
                </p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-0.5">
                <div class="bg-[#1B1B1C] w-[20rem] text-[#FFFFFFBF] p-3 rounded-2xl border hover:border-[#FF541F] hover:scale-105 transition ease-in">
                    <div class="flex flex-col gap-4">
                        <p>Free</p>
                        <p>
                            Everything you need to supercharge your
                            productivity.
                        </p>
                        <p>$0 / month</p>
                    </div>
                    <hr>
                    <div class="flex flex-col gap-4 mt-3">
                        <p>What's included</p>
                        <ul class="flex flex-col gap-1">
                            <li>20 design generations/month</li>
                            <li>Low-res downloads</li>
                            <li>Basic style presets</li>
                            <li>Limited customization options</li>
                        </ul>
                    </div>
                    <button 
                        class="px-6 py-2 rounded-xl border border-[#FF541F]/40 
                                bg-transparent text-white font-medium flex items-center gap-2
                                shadow-[0_0_25px_rgba(255,84,31,0.35)] 
                                hover:shadow-[0_0_35px_rgba(255,84,31,0.55)]
                                hover:bg-[#FF541F]
                                transition-all duration-300">
                        Subscribe
                        <span class="text-xl">›</span>
                    </button>
                </div>
                <div class="bg-[#1B1B1C] w-[20rem] text-[#FFFFFFBF] p-3 rounded-2xl border hover:border-[#FF541F] hover:scale-105 transition ease-in">
                    <div class="flex flex-col gap-4">
                        <p>Free</p>
                        <p>
                            Everything you need to supercharge your
                            productivity.
                        </p>
                        <p>$0 / month</p>
                    </div>
                    <hr>
                    <div class="flex flex-col gap-4 mt-3">
                        <p>What's included</p>
                        <ul class="flex flex-col gap-1">
                            <li>20 design generations/month</li>
                            <li>Low-res downloads</li>
                            <li>Basic style presets</li>
                            <li>Limited customization options</li>
                        </ul>
                    </div>
                    <button 
                        class="px-6 py-2 rounded-xl border border-[#FF541F]/40 
                                bg-transparent text-white font-medium flex items-center gap-2
                                shadow-[0_0_25px_rgba(255,84,31,0.35)] 
                                hover:shadow-[0_0_35px_rgba(255,84,31,0.55)]
                                hover:bg-[#FF541F]
                                transition-all duration-300">
                        Subscribe
                        <span class="text-xl">›</span>
                    </button>
                </div>
                <div class="bg-[#1B1B1C] w-[20rem] text-[#FFFFFFBF] p-3 rounded-2xl border hover:border-[#FF541F] hover:scale-105 transition ease-in">
                    <div class="flex flex-col gap-4">
                        <p>Free</p>
                        <p>
                            Everything you need to supercharge your
                            productivity.
                        </p>
                        <p>$0 / month</p>
                    </div>
                    <hr>
                    <div class="flex flex-col gap-4 mt-3">
                        <p>What's included</p>
                        <ul class="flex flex-col gap-1">
                            <li>20 design generations/month</li>
                            <li>Low-res downloads</li>
                            <li>Basic style presets</li>
                            <li>Limited customization options</li>
                        </ul>
                    </div>
                   <button 
                        class="px-6 py-2 rounded-xl border border-[#FF541F]/40 
                                bg-transparent text-white font-medium flex items-center gap-2
                                shadow-[0_0_25px_rgba(255,84,31,0.35)] 
                                hover:shadow-[0_0_35px_rgba(255,84,31,0.55)]
                                hover:bg-[#FF541F]
                                transition-all duration-300">
                        Subscribe
                        <span class="text-xl">›</span>
                    </button>

                        
                </div>
                
            </div>
        </div>
    </section>
</template>