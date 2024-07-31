<template>
  <div class="w-screen flex justify-center relative my-4">
    <p
      class="absolute top-5 text-3xl sm:text-4xl leading-tight font-serif text-slate-900"
    >
      {{ "Download CV" }}
    </p>
    <a href="/resume.pdf" download="VipulJain_CV">
      <img src="/public/dwnld.webp" @click="downloadResume()" id="cv" />
    </a>
  </div>
</template>
<script setup>
const downloadResume = () => {
  const img = document.getElementById("cv");
  img.src = "/dwnld.gif";
};
</script>
