<template>
  <div
    class="max-h-full max-w-full bg-slate-300 text-slate-900 font-serif px-12 py-12"
  >
    <div class="max-w-4xl mx-auto flex flex-col items-center">
      <h1 class="text-3xl sm:text-4xl leading-tight m-3">
        {{ "Relevant Courseworks" }}
      </h1>
      <div class="w-5/6 dummy">
        <Crousel :slides="slides" />
      </div>
    </div>
  </div>
</template>
<script setup>
const slides = ref([
  { url: "../AlgoToolbox.jpeg" },
  { url: "../Meta-FE.jpeg" },
  { url: "../adv-react.jpeg" },
  { url: "../PS_I.png" },
]);
</script>
<style>
.dummy {
  border: 2px solid black;
}
</style>
