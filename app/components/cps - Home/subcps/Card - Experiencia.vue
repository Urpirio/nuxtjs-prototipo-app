<script>
import { ArrowRight } from "lucide-vue-next";

export default {
  props: ["titulo", "image"],
};
</script>
<template>
  <article
    class="flex items-center justify-between min-w-90 max-w-100 backdrop-blur-xl p-3 rounded-2xl bg-white/20 border-2 border-gray-50/20"
  >
    <img class="w-1/2 rounded-xl" :src="image" :alt="titulo" />
    <div class="flex flex-col w-1/2 justify-between h-full px-2">
      <h3 class="text-xl text-white font-semibold text-wrap">{{ titulo }}</h3>
      <button
        class="bg-white rounded-md py-1 font-semibold hover:bg-white/80 duration-300 hover:scale-102 flex items-center justify-between px-5 py-2"
      >
        <span>Get Started</span>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="lucide lucide-arrow-right-icon lucide-arrow-right"
        >
          <path d="M5 12h14" />
          <path d="m12 5 7 7-7 7" />
        </svg>
      </button>
    </div>
  </article>
</template>
