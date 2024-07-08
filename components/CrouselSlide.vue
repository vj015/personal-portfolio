<template>
  <div>
    <Swiper
      :modules="[SwiperAutoplay, SwiperNavigation]"
      :slides-per-view="1"
      :loop="false"
      :navigation="true"
      :autoplay="{
        delay: 8000,
        disableOnInteraction: true,
      }"
    >
      <SwiperSlide v-for="(slide, idx) in slides" :key="idx">
        <div class="flex flex-col mx-10 md:mx-50">
          <p class="font-serif font-thin text-xl underline">
            {{ slide.title }}
          </p>
          <p class="font-serif text-xl my-2">
            {{ slide.content }}
          </p>
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
  width: 90%;
  height: 90%;
}

.swiper-cards .swiper-slide {
  border-radius: 6px;
  border: 1px solid black;
}
.swiper-button-next,
.swiper-button-prev {
  color: #0f172a !important;
}
.swiper-pagination-bullet-active {
  background-color: #0f172a !important;
}
</style>
