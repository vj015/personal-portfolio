<template>
  <div
    class="max-h-full max-w-full bg-slate-300 text-slate-900 font-serif md:px-12 py-12"
  >
    <div class="max-w-4xl mx-auto flex flex-col items-center">
      <h1 class="text-2xl sm:text-4xl leading-tight m-3">
        {{ "Relevant Courseworks" }}
      </h1>
      <div class="max-w-full md:w-5/6">
        <Crousel :slides="slides" />
      </div>
    </div>
  </div>
</template>
<script setup>
const slides = ref([
  { url: "../AlgoToolbox.webp" },
  { url: "../Meta-FE.webp" },
  { url: "../adv-react.webp" },
  { url: "../PS_I.webp" },
  { url: "../temporal.webp" },
]);
</script>
<style></style>
