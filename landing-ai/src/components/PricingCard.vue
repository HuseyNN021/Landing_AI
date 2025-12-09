<script setup>
const communitData=[
    {title: 'Title1', description: 'desc1'},
    {title: 'Title2', description: 'desc2'},
    {title: 'Title3', description: 'desc3'},
]
</script>

<template>
    <section>
           <div 
            class="
                flex overflow-x-auto snap-x snap-mandatory gap-4 px-4
                md:grid md:grid-cols-3 md:gap-6 md:overflow-visible
                items-center
                ">
                <div
                class="
                    min-w-[90%] snap-center
                    h-[22rem]
                    lg:h-[25rem]
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
                    min-w-[80%] snap-center
                    h-[22rem]
                    lg:h-[27rem]
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
                    min-w-[90%] snap-center
                    h-[22rem]
                    lg:h-[25rem]
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
            </div>

    </section>
</template>