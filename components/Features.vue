<template>
  <section class="max-w-7xl m-auto mt-24 md:mt-32">
    <div
      v-for="(feature, id) in features"
      :key="id"
      class="mt-16 flex flex-col lg:flex-row mx-auto w-[90%] xl:w-[69.4rem] rounded-[20px] bg-[#F9FAFB] md:gap-6 lg:g-0">
      <div class="flex flex-col p-4 md:p-0 md:pl-4 py-10 gap-4">
        <div
          class="flex flex-col-reverse md:flex-row gap-1 md:gap-2 w-[16rem] md:w-[26rem] md:items-center">
          <h2
            class="text-[#111827] text-[1.125rem] md:text-[2rem] font-[700] md:font-[600] leading-[2.5rem] tracking-[-0.36px] md:tracking-[-0.64px]">
            {{ feature.name }}
          </h2>
          <p
            v-if="feature.tag"
            class="bg-[#267DFF] px-2 py-1 rounded-2xl self-start text-white">
            {{ feature.tag }}
          </p>
        </div>

        <p
          class="md:w-[39rem] text-[0.875rem] md:text-[1.125rem] leading-[1.25rem] md:leading-[1.75rem] text-[#111827]">
          {{ feature.description }}
        </p>
        <ul class="list-outside list-image-checkmark ml-8">
          <li
            v-for="(item, id) in feature.items.split(',')"
            :key="id"
            class="text-[0.875rem] md:text-[1rem] leading-6 text-[#374151]">
            {{ item }}
          </li>
        </ul>
        <div class="flex flex-col md:flex-row gap-2 mt-4 self-start">
          <button class="bg-[#267DFF] text-white px-4 py-2 rounded-lg">
            {{ feature.btnA }}
          </button>
          <button
            v-if="feature.btnB"
            class="text-[#267DFF] px-4 py-2 rounded-lg">
            {{ feature.btnB }}
          </button>
        </div>
      </div>
      <div class="lg:w-[18rem] xl:w-1/2 shrink-0 h-full">
        <img :src="feature.img" alt="feature.name" />
      </div>
    </div>
  </section>
</template>

<script>
import { features } from "~/data/features.js";

export default {
  data() {
    return {
      features,
    };
  },
};
</script>
