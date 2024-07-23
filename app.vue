<template>
  <div>
    <Home />
    <Experience />
    <Skills />
    <Projects />
    <DownloadCV />
    <Footer />
  </div>
</template>

<script setup lang="ts">
import { useHead, useSeoMeta } from "#imports";

useHead({
  title: "Vipul Jain - Full Stack Developer",
  meta: [
    {
      name: "description",
      content:
        "Welcome to my portfolio! I'm Vipul Jain, a design-oriented full-stack software engineer specializing in Payments. With a passion for crafting elegant interfaces and scalable solutions, I bring creativity and technical expertise to every project. Explore my work and discover how I blend technology with design to create exceptional user experiences.",
    },
    {
      name: "keywords",
      content:
        "Vipul Jain, Vipul, Front End Developer, UI Developer, UI, Frontend, Payments, Vue JS, Nuxt JS, Spring Boot, Spring, Full Stack Developer, Software Engineer, Payments, Portfolio, Web Developer, UI/UX Design, Frontend, Backend",
    },
    { property: "og:title", content: "Vipul Jain - Full Stack Developer" },
    {
      property: "og:description",
      content:
        "Explore the work of Vipul Jain, a design-focused full-stack software engineer specializing in Payments. Discover elegant interfaces and scalable solutions that blend technology and design seamlessly.",
    },
    { property: "og:image", content: "https://vipuljain.in/pikachu.jpg" },
    { property: "og:url", content: "https://vipuljain.in" },
    { name: "twitter:card", content: "summary_large_image" },
    { name: "twitter:title", content: "Vipul Jain - Full Stack Developer" },
    {
      name: "twitter:description",
      content:
        "Explore the work of Vipul Jain, a design-focused full-stack software engineer specializing in Payments. Discover elegant interfaces and scalable solutions that blend technology and design seamlessly.",
    },
    { name: "twitter:image", content: "https://vipuljain.in/pikachu.jpg" },
  ],
  script: [
    {
      hid: "gtag",
      src: "https://www.googletagmanager.com/gtag/js?id=G-BPGF4E84TT",
      async: true,
    },
    {
      hid: "gtag-inline",
      innerHTML: `
        window.dataLayer = window.dataLayer || [];
        function gtag(){dataLayer.push(arguments);}
        gtag('js', new Date());
        gtag('config', 'G-BPGF4E84TT');
      `,
    },
  ],
});

useSeoMeta({
  ogTitle: "Vipul Jain - Full Stack Developer",
  description:
    "Welcome to my portfolio! I'm Vipul Jain, a design-oriented full-stack software engineer specializing in Payments. With a passion for crafting elegant interfaces and scalable solutions, I bring creativity and technical expertise to every project. Explore my work and discover how I blend technology with design to create exceptional user experiences.",
  ogDescription:
    "Explore the work of Vipul Jain, a design-focused full-stack software engineer specializing in Payments. Discover elegant interfaces and scalable solutions that blend technology and design seamlessly.",
  ogImage: "https://vipuljain.in/pikachu.jpg",
  ogUrl: "https://vipuljain.in",
});
</script>
