<script setup>

import Button from '@/Reuseable/Button.vue';
</script>

<template>

    <header class="p-3">
        <section class="w-full flex justify-around items-center">
            <img class="w-[3.3rem] h-[2.5rem]" src="../assets/Images/Logo (8).png" alt="logo">
            <ul class="hidden md:flex lg:flex flex gap-7 text-white">
                <li class="nav-item"><a href="">Home</a></li>
                <li class="nav-item"><a href="">Services</a></li>
                <li class="nav-item"><a href="">Contact us</a></li>
                <li class="nav-item"><a href="">About us</a></li>
            </ul>
            <Button :text="'Login'"/>
        </section>
    </header>

</template>
<style scoped>

.nav-item {
  position: relative;
  display: inline-block;
  cursor: pointer;
}

/* underline line */
.nav-item::after {
  content: "";
  position: absolute;
  bottom: -2px;      /* -0.5 => 2px */
  left: 0;
  width: 0;
  height: 2px;       /* h-0.5 => 2px */
  background-color: #FF541F; /* bg-yellow-200 */
  transition: width 0.3s ease;
}

/* hover effect */
.nav-item:hover::after {
  width: 100%;
}

.nav-item:hover{
    cursor: pointer;
}
</style>