<template>
  <section class="p-4">
    <h1 class="text-4xl p-4 text-center">Vue3-Radio-Card Demo</h1>
    <div class="light mb-4">
      <!-- component -->
      <p class="text-sm text-center">Example with item slot</p>
      <radio-card v-model="selected" :options="items" title="Light mode">
        <template #item="{ value, price }">
          <span class="font-bold text-gray-900">
            <span class="text-4xl">{{ value }}</span>
          </span>
          <span>
            <span class="text-xl font-bold text-gray-500">$</span>
            <span class="text-xl font-bold text-gray-900 -ml-1"
              >&nbsp;{{ price }}</span
            >
            <span class="text-xl font-semibold text-gray-500">/</span>
            <span class="text-lg font-semibold text-gray-500">mo</span>
          </span>
        </template>
      </radio-card>
    </div>
    <div class="dark mt-4">
      <!-- component -->
      <p class="text-sm text-center">Example without slot</p>

      <radio-card v-model="selected" :options="items" title="Dark mode">
      </radio-card>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import { RadioCard } from "vue3-radio-card";
import "vue3-radio-card/style.css";
const selected = ref();

const items = [
  { label: "50 GB", value: "50", price: 5 },
  { label: "80 GB", value: "80", price: 7 },
  { label: "100 GB", value: "100", price: 10 },
  { label: "200 GB", value: "200", price: 18 },
];
</script>

<style></style>
