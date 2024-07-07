<template>
  <div>
    <Swiper
      :modules="[
        SwiperAutoplay,
        SwiperNavigation,
        SwiperPagination,
        SwiperEffectCards,
      ]"
      :slides-per-view="1"
      :loop="false"
      :effect="'cards'"
      :navigation="true"
      :pagination="true"
      :autoplay="{
        delay: 8000,
        disableOnInteraction: true,
      }"
    >
      <SwiperSlide v-for="(slide, idx) in slides" :key="idx">
        <div>
          <img :src="`${slide.url}`" />
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
  width: 80%;
  height: 90%;
}

.swiper-cards .swiper-slide {
  border-radius: 6px;
  border: 1px solid black;
}
</style>
