<script setup>
import { ref, reactive, computed } from "vue";
import BaseIcon from "./BaseIcon.vue";

const model = reactive({
  Reaction: "Reaction",
  Memory: "Memory",
  Verbal: "Verbal",
  Visual: "Visual",
});
</script>

<template>
  <div class="flex items-center justify-center h-screen bg-slate-100">
    <div
      class="flex flex-col md:flex-row h-full md:h-auto md:w-2/5 lg:w-2/5 2xl:w-4/12 bg-white rounded-xl shadow-2xl"
    >
      <div
        class="flex flex-col pt-6 items-center bg-[#5A3DF9] rounded-b-3xl md:rounded-xl pb-8 md:pb-12 text-slate-300 text-center w-full"
      >
        <h1 class="pb-6 text-lg font-medium">Your Result</h1>

        <div
          class="flex flex-col justify-center bg-[#3A2FED] w-32 h-32 md:w-32 md:h-32 rounded-full bg-opacity-80 shadow-2xl"
        >
          <span class="text-white text-5xl font-bold">76 </span>
          <span class="pt-2 text-xs opacity-50">of 100 </span>
        </div>

        <div class="flex flex-col px-20 md:px-9 pt-5">
          <h2 class="text-white text-xl font-semibold">Great</h2>
          <span class="text-xs md:text-sm font-medium pt-4">
            You scored higher than 65% of the people who have taken these tests.
          </span>
        </div>
      </div>

      <div class="flex flex-col bg-white rounded-xl px-8 py-5 md:p-5 w-full">
        <span class="font-bold text-xl pb-3">Summary</span>

        <div class="flex items-center relative justify-between py-3 pb-6">
          <!-- <BaseIcon :avatar="index.icon" :username="index.category" /> -->
          <img class="pl-2" src="../assets/images/icon-reaction.svg" alt="" />

          <input
            v-model="model.Reaction"
            class="text-[#FF5555] bg-[#FF5555] bg-opacity-10 font-bold absolute w-full px-10 py-2 pr-14 appearance-none rounded-md border border-gray-300 shadow-sm placeholder-gray-500 focus:z-10 focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm md:text-base"
          />
          <span class="text-xs text-[#FF5555] mr-2">
            <strong>80</strong> /100</span
          >
        </div>

        <div class="flex items-center relative justify-between py-3 pb-6">
          <!-- <BaseIcon :avatar="index.icon" :username="index.category" /> -->
          <img class="pl-2" src="../assets/images/icon-memory.svg" alt="" />
          <input
            v-model="model.Memory"
            class="text-[#FFB21E] bg-[#FFB21E] bg-opacity-10 font-bold absolute w-full px-10 py-2 pr-14 appearance-none rounded-md border border-gray-300 shadow-sm placeholder-gray-500 focus:z-10 focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm md:text-base"
          />
          <span class="text-xs text-[#FFB21E] mr-2">
            <strong>92</strong> /100</span
          >
        </div>

        <div class="flex items-center relative justify-between py-3 pb-6">
          <!-- <BaseIcon :avatar="index.icon" :username="index.category" /> -->
          <img class="pl-2" src="../assets/images/icon-verbal.svg" alt="" />

          <input
            v-model="model.Verbal"
            class="text-[#00BB8F] bg-[#00BB8F] bg-opacity-10 font-bold absolute w-full px-10 py-2 pr-14 appearance-none rounded-md border border-gray-300 shadow-sm placeholder-gray-500 focus:z-10 focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm md:text-base"
          />
          <span class="text-xs text-[#00BB8F] mr-2">
            <strong>61</strong> /100</span
          >
        </div>

        <div class="flex items-center relative justify-between py-3">
          <!-- <BaseIcon :avatar="index.icon" :username="index.category" /> -->
          <img class="pl-2" src="../assets/images/icon-visual.svg" alt="" />
          <input
            v-model="model.Visual"
            class="text-[#1125D6] bg-[#1125D6] bg-opacity-10 font-bold absolute w-full px-10 py-2 pr-14 appearance-none rounded-md border border-gray-300 shadow-sm placeholder-gray-500 focus:z-10 focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm md:text-base"
          />
          <span class="text-xs text-[#1125D6] mr-2">
            <strong>72</strong> /100</span
          >
        </div>

        <button
          class="rounded-full mt-5 bg-[#303B59] md:bg-indigo-700 md:hover:bg-indigo-600 shadow-md hover:font-bold w-full p-3 md:p-2 text-white font-semibold"
        >
          Continue
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
