<!-- <script setup>
import { ref } from 'vue';
const toggle=ref(true)
const toggleButton=()=>{
    toggle.value=!toggle.value
}
</script>

<template>

    <section>
        <div>
            
            <div class="text-white">
                <div>
                    <p>Question </p>
                    <p :class="toggle?'hidden':'block'">Answer</p>
                    <button @click="toggleButton">Clik</button>
                </div>
                <div>
                    <p>Question </p>
                    <p :class="toggle?'hidden':'block'">Answer</p>
                    <button @click="toggleButton">Clik</button>
                </div>
            </div>
        </div>
    </section>
</template> -->
<script setup>
import { ref } from "vue";

const faq = ref([
  {
    q: "How does the platform work?",
    a: "Our platform uses advanced algorithms to deliver personalized results.",
    open: false,
  },
  {
    q: "Can I change my plan anytime?",
    a: "Yes, you can upgrade or downgrade your plan at any time from your dashboard.",
    open: false,
  },
  {
    q: "Is there a free trial?",
    a: "Absolutely! We offer a 7-day free trial for all new users.",
    open: false,
  },
]);

const toggle = (index) => {
  faq.value[index].open = !faq.value[index].open;
};
</script>

<template>
  <section class="text-white w-full max-w-3xl mx-auto mt-10">
    <div>
        <h2 class="font-bold text-[2rem] md:text-[2.5rem] lg:text-[4rem] text-white w-[20rem] md:w-[29rem] lg:w-[37.5rem]">
            Frequently Asked Questions
        </h2>
        <p class="text-[0.7rem] md:text-[1rem] lg:text-[1.25rem] text-[#D9D9D9] w-[25rem] md:w-[37rem] lg:w-[48rem]">
            Got questions? We've got answers. Find everything you need to know about using our platform, plans, and features.
        </p>
    </div>
    <div
      v-for="(item, i) in faq"
      :key="i"
      class="border-b border-white/20 py-4"
    >
      <!-- Question -->
      <button
        @click="toggle(i)"
        class="w-full flex justify-between items-center"
      >
        <p class="text-xl font-semibold">{{ item.q }}</p>

        <!-- Icon (rotates) -->
        <span
          class="text-2xl transform transition-all duration-300 p-1"
          :class="item.open ? 'rotate-90' : 'rotate-0'"
        >
          ›
        </span>
      </button>

      <!-- Answer with smooth slide animation -->
      <transition name="slide">
        <p
          v-if="item.open"
          class="mt-2 text-gray-300 text-sm leading-relaxed"
        >
          {{ item.a }}
        </p>
      </transition>
    </div>

  </section>
</template>

<style scoped>
.slide-enter-from,
.slide-leave-to {
  opacity: 0;
  transform: translateY(-6px);
}

.slide-enter-to,
.slide-leave-from {
  opacity: 1;
  transform: translateY(0);
}

.slide-enter-active,
.slide-leave-active {
  transition: all 0.25s ease;
}
</style>
