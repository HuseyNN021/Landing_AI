<script setup>
import Button from '@/Reuseable/Button.vue';
</script>

<template>
    <section class="w-full">
        <div class="flex justify-center items-center">
            <div class="flex flex-col justify-center items-center gap-3 border border-amber-50 p-1">
                <h2 class="font-bold text-[2rem] md:text-[2.5rem] lg:text-[4rem] text-white w-[20rem] md:w-[29rem] lg:w-[50rem]">
                    Ready to Design Smarter?
                </h2>
                <p class="text-[0.7rem] md:text-[1rem] lg:text-[1.25rem] text-[#D9D9D9] w-[25rem] md:w-[37rem] lg:w-[48rem]">
                    Whether you're a freelancer, a team, or a growing agency—our tools adapt to your workflow. Design faster. Deliver better.       
                </p>
                <Button :text="'Get Started →'"/>
            </div>
        </div>
    </section>
</template>