<template>
  <div>
    <Swiper
      :modules="[SwiperAutoplay, SwiperNavigation, SwiperPagination]"
      :slides-per-view="1"
      :loop="true"
      effect="creative"
      :navigation="true"
      :pagination="true"
      :autoplay="{
        delay: 8000,
        disableOnInteraction: true,
      }"
    >
      <SwiperSlide v-for="(slide, idx) in slides" :key="idx">
        <div v-if="slide.url.length > 0">
          <img :src="`${slide.url}`" />
        </div>
        <div v-else>
          <iframe
            src="https://leetcode-badge-showcase.vercel.app/api?username=vj_015"
          ></iframe>
        </div>
      </SwiperSlide>
    </Swiper>
  </div>
</template>

<script setup>
const props = defineProps({
  slides: {
    type: Array,
    required: true,
  },
});

const { slides } = toRefs(props);
</script>

<style>
.swiper-slide {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 18px;
  height: 100%;
  font-size: 4rem;
  font-weight: bold;
  font-family: "Roboto", sans-serif;
}

.swiper-wrapper {
  width: 100%;
}

.swiper-cards {
  width: 240px;
  height: 240px;
}

.swiper-cards .swiper-slide {
  border-radius: 6px;
  border: 1px solid black;
}
</style>
