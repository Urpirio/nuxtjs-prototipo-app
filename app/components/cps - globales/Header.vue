<script setup>
import { Navegacion } from "~/data/Data - Navegacion";
const route = useRoute();
const handle_Logo = () => {
  window.location.href = "/";
};
</script>

<template>
  <header
    class="flex items-center justify-between py-5 px-10 fixed z-40 w-full"
  >
    <div class=" rounded-md p-3 backdrop-blur-xl ">
      <h1 @click="handle_Logo" class="cursor-pointer hover:scale-102 duration-300 text-3xl font-bold text-white">LOGO</h1>
    </div>
    <div
      id="navegacion"
      class="flex gap-5 bg-white/20 py-2 px-3 rounded-2xl font-bold backdrop-blur-xl"
    >
      <button
        v-for="(value, index) in Navegacion"
        :key="index"
        :class="
          value.pathname == route.path
            ? 'bg-gray-500/50 text-white  px-2 py-2 rounded-md'
            : 'bg-none  px-5 py-2 rounded-md text-white'
        "
      >
        <a :href="value.pathname">{{ value.label }}</a>
      </button>
    </div>
  </header>
</template>
