<script setup>
import { defineProps } from 'vue';

const props=defineProps({
    text: {
        type: String,
    }
})
</script>

<template>
    <button 
    class="
    bg-[#FF541F]
    rounded-[10px]
    w-[80px]
    md:w-[100px]
    lg:w-[120px]
    h-[35px]
    md:h-[40px]
    lg:h-[50px]
    p-1
    text-white
    flex
    justify-center
    items-center
    cursor-pointer
    ">
        <span class="text-[0.5rem] md:text-[1rem] ">{{ props.text }}</span>
    </button>
</template>