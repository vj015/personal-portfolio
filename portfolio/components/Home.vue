<template>
  <div class="bg-slate-900 text-slate-300 font-sans flex flex-col md:flex-row h-screen">
    <div class="main px-8 md:px-16 py-12 flex-1">
      <div class="main__header py-10 text-3xl sm:text-4xl leading-tight">
        <span>{{ "Hello!" }}</span>
        <span>
          <img src="/wave.png" alt="Hello" class="w-10 sm:w-12 mx-2" />
        </span>
      </div>
      <div class="main__body py-10 text-3xl sm:text-4xl md:text-5xl leading-tight">
        <span>{{ "I'm " }}</span>
        <span class="font-extrabold">{{ "Vipul Jain" }}</span>
        <span>
          {{ ", a design-minded front-end heavy full stack software engineer focused on building beautiful interfaces, scalable services & experiences" }}
        </span>
        <span>
          <img src="/technologist.png" alt="Technologist" class="w-10 sm:w-12 mx-2" />
        </span>
      </div>
      <div class="main__footer py-10 text-2xl sm:leading-tight">
        <span>{{ "Get in touch" }}</span>
        <span>
          <img src="/pointright.png" alt="Pointing Right" class="w-6 mx-2" />
        </span>
        <span class="highlight_link">
          <a href="mailto:vjain2376@gmail.com" target="_blank">{{ "vjain2376@gmail.com" }}</a>
        </span>
      </div>
    </div>
    <div class="flex flex-row md:flex-col mx-0 pr-16 py-12 justify-evenly items-center space-y-4 md:space-y-8">
      <div class="flex flex-col items-center">
        <div class="font-mono text-3xl md:text-4xl">{{ animatedLines }}</div>
        <div class="font-semibold text-center">
          <span class="text-2xl">{{ "lines of code " }}</span>
          <span class="text-3xl">{{ "</>" }}</span>
        </div>
      </div>
      <div class="flex flex-col items-center">
        <div class="font-mono text-3xl md:text-4xl">{{ animatedPixels }}</div>
        <div class="font-semibold text-center">
          <span class="text-2xl">{{ "pixels rendered " }}</span>
          <span class="text-3xl">{{ "🚀" }}</span>
        </div>
      </div>
      <div class="flex flex-col items-center">
        <div class="font-mono text-3xl md:text-4xl">{{ animatedCups }}</div>
        <div class="font-semibold text-center">
          <span class="text-2xl">{{ "cups of coffee drunk " }}</span>
          <span class="text-3xl">{{ "☕︎" }}</span>
        </div>
      </div>
      <div class="flex flex-col items-center">
        <div class="font-mono text-3xl md:text-4xl">{{ animatedProjects }}</div>
        <div class="font-semibold text-center">
          <span class="text-2xl">{{ "projects completed " }}</span>
          <span class="text-3xl">{{ "🛠️" }}</span>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
import { ref, onMounted } from 'vue';

const finalLines = 134566;
const finalPixels = 301783509;
const finalCups = 1400;
const finalProjects = 26;

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
  animateNumber(finalLines, animatedLines);
  animateNumber(finalPixels, animatedPixels);
  animateNumber(finalCups, animatedCups);
  animateNumber(finalProjects, animatedProjects);
});
</script>
<style scoped>
.main {
  max-width: 800px;
  margin: 0 auto;
  flex-direction: column;
  justify-content: space-between;
}
@keyframes wave {
  from {
    transform: none;
  }
  15% {
    transform: translate3d(-20%, 0, 0) rotate3d(0, 0, 1, -10deg);
  }
  30% {
    transform: translate3d(10%, 0, 0) rotate3d(0, 0, 1, 7deg);
  }
  45% {
    transform: translate3d(-15%, 0, 0) rotate3d(0, 0, 1, -10deg);
  }
  60% {
    transform: translate3d(10%, 0, 0) rotate3d(0, 0, 1, 5deg);
  }
  75% {
    transform: translate3d(-5%, 0, 0) rotate3d(0, 0, 1, -2deg);
  }
  to {
    transform: none;
  }
}
.main img {
  display: inline-block;
  vertical-align: bottom;
  animation: none;
  cursor: pointer;
}
.main__header img:hover {
  animation: wave 1s both;
}
.main__body {
  max-width: 725px;
}
.highlight_link:hover {
  transition: all 0.2s ease-in-out;
  font-weight: 400;
  text-decoration: underline;
  color: #0f172a;
  background-color: rgb(255, 207, 76);
  box-shadow: inset 0 -3px 0 rgb(255, 207, 76);
  padding: 2px 3px;
}
</style>
