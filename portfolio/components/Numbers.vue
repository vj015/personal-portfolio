<template>
    <div class="flex flex-row md:flex-col items-center py-5 md:py-10 md:px-20 flex-nowrap">
      <div class="flex flex-col items-center m-2 sm:m-3 md:m-6">
        <div class="font-mono font-extrabold sm:text-3xl md:text-4xl">{{ animatedLines }}</div>
        <div class="font-serif md:font-semibold text-center">
          <span class="sm:text-2xl">{{ "lines of code " }}</span>
          <span class="sm:text-3xl">{{ "</>" }}</span>
        </div>
      </div>
      <div class="flex flex-col items-center m-2 sm:m-3 md:m-6">
        <div class="font-mono font-extrabold sm:text-3xl md:text-4xl">{{ animatedPixels }}</div>
        <div class="font-serif md:font-semibold text-center">
          <span class="sm:text-2xl">{{ "pixels rendered " }}</span>
          <span class="sm:text-3xl">{{ "🚀" }}</span>
        </div>
      </div>
      <div class="flex flex-col items-center m-2 sm:m-3 md:m-6">
        <div class="font-mono font-extrabold sm:text-3xl md:text-4xl">{{ animatedCups }}</div>
        <div class="font-serif md:font-semibold text-center">
          <span class="sm:text-2xl">{{ "cups of coffee drunk " }}</span>
          <span class="sm:text-3xl">{{ "☕︎" }}</span>
        </div>
      </div>
      <div class="flex flex-col items-center m-2 sm:m-3 md:m-6">
        <div class="font-mono font-extrabold sm:text-3xl md:text-4xl">{{ animatedProjects }}</div>
        <div class="font-serif md:font-semibold text-center">
          <span class="sm:text-2xl">{{ "projects completed " }}</span>
          <span class="sm:text-3xl">{{ "🛠️" }}</span>
        </div>
      </div>
    </div>
</template>
<script setup>
import { ref, onMounted } from 'vue';

const animatedLines = ref(0);
const animatedPixels = ref(0);
const animatedCups = ref(0);
const animatedProjects = ref(0);

const animateNumber = (target, refVar, duration = 2000) => {
  const start = 0;
  const increment = Math.max(1, target / (duration / 10));
  const step = () => {
    refVar.value = Math.min(target, Math.floor(refVar.value + increment));
    if (refVar.value < target) {
      setTimeout(step, 10);
    } else {
      refVar.value = target;
    }
  };
  step();
};
onMounted(() => {
  animateNumber(134566, animatedLines);
  animateNumber(301783509, animatedPixels);
  animateNumber(1400, animatedCups);
  animateNumber(26, animatedProjects);
});
</script>