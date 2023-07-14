<script setup>
import { ref, reactive, computed } from "vue";
import BaseIcon from "./BaseIcon.vue";
import data from "../data.js";

const model = reactive(data);
</script>

<template>
  <div class="flex items-center justify-center h-screen bg-red-200">
    <div
      class="flex flex-col md:flex-row h-full md:h-auto md:w-2/5 bg-white rounded-xl"
    >
      <div
        class="flex flex-col pt-6 items-center bg-[#5A3DF9] rounded-b-3xl md:rounded-xl pb-8 text-slate-300 text-center w-full"
      >
        <h1 class="pb-5 text-lg">Your Result</h1>

        <div
          class="flex flex-col justify-center bg-[#3A2FED] w-32 h-32 md:w-32 md:h-32 rounded-full bg-opacity-80 "
        >
          <span class="text-white text-5xl font-bold">76 </span>
          <span class="pt-2 text-xs opacity-50  ">of 100 </span>
        </div>

        <div class="flex flex-col px-20 md:px-11 pt-5">
          <h2 class="text-white text-xl font-semibold">Great</h2>
          <span class="text-xs font-medium pt-3">
            You scored higher than 65% of the people who have taken these tests.
          </span>
        </div>
      </div>

      <div class="flex flex-col bg-white rounded-xl px-8 md:p-5 py-6 w-full">
        <h1 class="font-bold pb-3">Summary</h1>
        <div
          class="flex items-center relative justify-between py-3 md:py-2"
          v-for="(index, item) in model"
          :key="item"
        >
          <BaseIcon :avatar="index.icon" :username="index.category" />

          <input
            v-model="index.category"
            class=" bg-opacity-5 font-bold absolute w-full px-10 py-2 pr-14 appearance-none rounded-md border border-gray-300 shadow-sm placeholder-gray-500 focus:z-10 focus:border-indigo-500 focus:outline-none focus:ring-indigo-500 sm:text-sm"
            :class="index.textColor"
          />
          <span class="text-xs mr-2">
            <strong>{{ index.score }}</strong> /100</span
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
