<template>
  <section class="max-w-7xl m-auto mt-24 md:mt-32">
    <h1
      class="text-center shrink-0 text-[1.125rem] md:text-[2.25rem] text-[#111827] font-[700] leading-[1.5rem] md:leading-[2.75rem] tracking-[-0.36px] md:tracking-[-0.72px]">
      Feature Articles
    </h1>
    <div class="w-[90%] flex flex-col md:flex-row items-center mx-auto gap-4">
      <div
        v-for="(article, id) in articles"
        :key="id"
        class="h-[26.5rem] flex flex-col justify-start items-center mt-6 md:mt-10 rounded-xl shadow-lg">
        <img :src="article.img" alt="article.name" class="h-[13.5rem]" />
        <div class="flex flex-col items-center gap-2 lg:gap-4 p-5">
          <h1
            class="text-[1.125rem] lg:text-[1.25rem] text-[#111827] font-[800] md:font-[700] leading-[1.75rem] md:leading-[1.75rem] tracking-[-0.36px] md:tracking-[-0.4px]">
            {{ article.title }}
          </h1>
          <p
            class="text-[0.875rem] lg:text-[1rem] text-[#374151] md:text-[#6B7280] leading-6 h-auto">
            {{ article.preview }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { articles } from "~/data/articles.js";

export default {
  data() {
    return {
      articles,
    };
  },
};
</script>
