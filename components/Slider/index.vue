<template>
  <section class="slider-container">
    
    <div id="slider" class="slider">
        <div v-for="slider in sliders" class="slider-item">
          <img :src="slider.image" alt="" />
        </div>
      </div>

    <button
      id="prevBtn"
      @click="prevSlide"
      class="round bg-[#e5e5e5] px-3 py-2 rounded text-black mr-3"
    >
      Previous
    </button>
    <button
      id="nextBtn"
      @click="nextSlide"
      class="round bg-[#e5e5e5] px-3 py-2 rounded text-black"
    >
      Next
    </button>
  </section>
</template>
<script setup>
const props = defineProps({
  sliders: {
    type: Array,
    required: true,
  },
  itemsPerSlide: {
    type: Number,
    default: 3,
  },
});
onMounted(() => {});

const nextSlide = () => {
  let slider = document.getElementById("slider");
  let itemWidth = slider.querySelector(".slider-item").offsetWidth + 10;
  slider.scrollBy({
    left: itemWidth*props.itemsPerSlide,
    behavior: "smooth",
  });
};
const prevSlide = () => {
  let slider = document.getElementById("slider");
  let itemWidth = slider.querySelector(".slider-item").offsetWidth + 10;
  slider.scrollBy({
    left: -itemWidth*props.itemsPerSlide,
    behavior: "smooth",
  });
};
</script>
<style scoped>
.slider-container {
  position: relative;
  width: 100%;
  overflow: hidden;
}
.slider {
  display: flex;
  overflow-x: scroll;
  scroll-behavior: smooth;
  scrollbar-width: none; /* Firefox */
  -ms-overflow-style: none; /* IE 10+ */
  touch-action: pan-x;
}
.slider-item {
  flex: 0 0 18.25%;
  box-sizing: border-box;
  padding: 10px;
}
.slider-item:first-child,
.slider-item:last-child {
  flex-basis: calc(18.25% + 3.5vw + 14px);
}
.slider-item:first-child {
  padding-left: calc(3.5vw + 24px);
}
.slider-item:last-child {
  padding-right: calc(3.5vw + 24px);
}

.scroll {
  overflow-x: scroll;
  scroll-behavior: smooth;
  scrollbar-width: none;
  touch-action: pan-x;
}
</style>
