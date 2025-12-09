<script setup>

import Button from '@/Reuseable/Button.vue';
import { onMounted } from 'vue';
import { gsap } from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'
// ScrollToPlugin kaydırma animasiyası üçün vacibdir.
import ScrollToPlugin from 'gsap/ScrollToPlugin' 

gsap.registerPlugin(ScrollTrigger, ScrollToPlugin) 
// ☝️ ScrollToPlugin-i qeydiyyatdan keçirməyi unutmayın!

// ----------------------------------------------------------------
// Yeni Hamar Kaydırma (Smooth Scroll) Funksiyası
// ----------------------------------------------------------------
function scrollToElement(id) {
    gsap.to(window, {
        duration: 1.2, // 👈 Animasiyanın sürəti (saniyə)
        ease: "power2.inOut", // Animasiyanın növü
        scrollTo: {
            y: `#${id}`, // Hədəf ID-yə kaydır
            offset: 0 // Hədəfdən neçə piksel yuxarıda dayanmaq (məsələn, sabit nav üçün)
        }
    });
}
// ----------------------------------------------------------------


onMounted(() => {
    // Sizin mövcud GSAP ScrollTrigger animasiyanız
    gsap.from('.wrapper > div', {
        scrollTrigger: {
            trigger: "#scrollId",
            start: "top 85%",
            toggleActions: "play none none none"
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

    <header id="headerID" class="p-3">
        <section class="w-full flex justify-around items-center">
            <img class="w-[3.3rem] h-[2.5rem]" src="../assets/Images/Logo (8).png" alt="logo">
            <ul class="hidden md:flex lg:flex flex gap-7 text-white">
                <li class="nav-item"><a href="#" @click.prevent="">Home</a></li>
                <li class="nav-item"><a href="#"  @click.prevent="scrollToElement('faqSection')">Services</a></li>
                <li class="nav-item"><a href="#"  @click.prevent="scrollToElement('pricingNav')">Contact us</a></li>
                <li class="nav-item"><a href="#" @click.prevent="scrollToElement('ctaNav')">About us</a></li>
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