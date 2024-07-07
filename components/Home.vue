<template>
  <div
    class="bg-slate-900 text-slate-300 font-sans flex flex-col md:flex-row max-h-full max-w-full px-12 py-3 md:py-12 items-center"
  >
    <div class="flex flex-col justify-between items-center md:items-start font-serif">
      <div class="main__header py-10 text-3xl sm:text-4xl leading-tight">
        <span>{{ "Hello!" }}</span>
        <span>
          <img src="/wave.png" alt="Hello" class="w-10 sm:w-12 mx-2 inline-block align-bottom cursor-pointer" />
        </span>
      </div>
      <div
        class="max-w-4xl py-10 text-3xl sm:text-4xl md:text-5xl leading-tight"
      >
        <span>{{ "I'm " }}</span>
        <span class="font-extrabold">{{ "Vipul Jain" }}</span>
        <span>
          {{
            ", a design-minded front-end heavy full stack software engineer currently working in Payments and focused on building beautiful interfaces, scalable services & experiences"
          }}
        </span>
        <span>
          <img
            src="/technologist.png"
            alt="Technologist"
            class="w-10 sm:w-12 mx-2 inline-block align-bottom cursor-pointer"
          />
        </span>
      </div>
      <div class="main__footer py-10 text-2xl sm:leading-tight">
        <span>{{ "Get in touch" }}</span>
        <span>
          <img src="/pointright.png" alt="Pointing Right" class="w-6 mx-2 inline-block align-bottom cursor-pointer" />
        </span>
        <span class="highlight_link">
          <a href="mailto:vjain2376@gmail.com" target="_blank">{{
            "vjain2376@gmail.com"
          }}</a>
        </span>
      </div>
    </div>
    <div class="">
      <Numbers />
    </div>
  </div>
</template>
<style scoped>
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
.main__header img:hover {
  animation: wave 1s both;
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
