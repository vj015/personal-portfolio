<template>
  <div class="bg-slate-900 text-slate-300 font-sans main px-16 py-12">
    <div
      class="main__header py-10 text-3xl leading-tight sm:leading-tight sm:text-4xl"
    >
      <span>{{ "Hello!" }}</span>
      <span>
        <img src="../public/wave.png" alt="Hello" class="w-10 sm:w-12 mx-2"
      /></span>
    </div>
    <div
      class="main__body py-10 text-3xl leading-tight sm:leading-tight sm:text-4xl md:text-5xl"
    >
      <span>{{ "I'm " }}</span
      ><span class="font-extrabold">{{ "Vipul Jain" }}</span
      ><span>
        {{
          ", a design-minded front-end heavy full stack software engineer focused on building beautiful interfaces, scalable services & experiences"
        }}</span
      >
      <span>
        <img src="../public/technologist.png" alt="" class="w-10 sm:w-12 mx-2"
      /></span>
    </div>
    <div class="main__footer py-10 text-2xl sm:leading-tight">
      <span>{{ "Get in touch" }}</span>
      <span>
        <img src="../public/pointright.png" alt="" class="w-6 mx-2"
      /></span>
      <span class="highlight_link">
        <a href="mailto:vjain2376@gmail.com" target="_blank">{{
          "vjain2376@gmail.com"
        }}</a>
      </span>
    </div>
  </div>
</template>
<style>
.main {
  display: flex;
  justify-content: space-between;
  margin: 0 auto;
  flex-direction: column;
  height: 100vh;
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
@-webkit-keyframes wave {
  from {
    -webkit-transform: none;
  }
  15% {
    -webkit-transform: translate3d(-20%, 0, 0) rotate3d(0, 0, 1, -10deg);
  }
  30% {
    -webkit-transform: translate3d(10%, 0, 0) rotate3d(0, 0, 1, 7deg);
  }
  45% {
    -webkit-transform: translate3d(-15%, 0, 0) rotate3d(0, 0, 1, -10deg);
  }
  60% {
    -webkit-transform: translate3d(10%, 0, 0) rotate3d(0, 0, 1, 5deg);
  }
  75% {
    -webkit-transform: translate3d(-5%, 0, 0) rotate3d(0, 0, 1, -2deg);
  }
  to {
    -webkit-transform: none;
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
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  font-weight: 400;
  text-decoration: underline;
  color: #0f172a;
  display: inline-block;
  padding: 2px 3px;
  background-color: rgb(255 207 76);
  -webkit-box-shadow: inset 0 -3px 0 rgb(255 207 76);
  box-shadow: inset 0 -3px 0 rgb(255 207 76);
}
</style>
