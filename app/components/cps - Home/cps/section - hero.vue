<script setup>
import { Facebook } from "lucide-vue-next";
import { Instagram } from "lucide-vue-next";
import { Bird } from "lucide-vue-next";
import CardExperiencia from "../subcps/Card - Experiencia.vue";
import { Experiencia } from "~/data/Data - Experiencia";
</script>

<template>
  <section class="relative flex flex-col h-screen">
    <img
      src="https://i.pinimg.com/1200x/47/da/2d/47da2d09a9bb2394dd764adc789ab193.jpg"
      alt="Una Imagen"
      class="w-full h-full"
    />
    <div class="absolute w-full top-40 px-10 flex flex-col gap-20   ">
      <div>
        <div class="text-start space-y-5">
          <h2 class="text-2xl text-white font-semibold">
            More power Efficiency
          </h2>
          <p class="text-8xl text-white font-bold">
            Experience the future <br />
            of Solar Power.
          </p>
          <button
            class="border rounded-xl bg-white px-5 py-3 text-xl font-semibold"
          >
            <div>Get Stared</div>
          </button>
        </div>
        <div class="flex items-center py-5 gap-3">
          <button
            class="border-2 border-gray-300/20 p-3 rounded-full text-white backdrop-blur-xl hover:scale-105"
          >
            <Facebook />
          </button>
          <button
            class="border-2 border-gray-300/20 p-3 rounded-full text-white backdrop-blur-xl hover:scale-105"
          >
            <Instagram />
          </button>
          <button
            class="border-2 border-gray-300/20 p-3 rounded-full text-white backdrop-blur-xl hover:scale-105"
          >
            <Bird />
          </button>
        </div>
      </div>
      <div class="flex gap-5 py-5 ">
        <CardExperiencia
          v-for="(value, index) in Experiencia"
          :key="index"
          :titulo="value.titulo"
          :image="value.image"
        />
      </div>
    </div>
  </section>
</template>
