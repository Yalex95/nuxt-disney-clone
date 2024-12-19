<template>
  <div class="slider-container py-[10px]">
    <div id="slider" class="slider">
      <div v-for="slider in sliders" class="slider-item ">
        <img :src="slider.image" :alt="slider.alt" />
      </div>
    </div>

    <div class="controls">
      <button
        id="prevBtn"
        @click="prevSlide"
        :class="[
          showPrevArrow ? 'active' : '',
          'round  px-3 py-2 rounded text-black mr-3',
        ]"
      >
        <span
          ><svg
            xmlns="http://www.w3.org/2000/svg"
            class="button-icon"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
            aria-label="previous button"
            role="img"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M15 19l-7-7 7-7"
            ></path></svg
        ></span>
      </button>
      <button
        id="nextBtn"
        @click="nextSlide"
        :class="[
          showNextArrow ? 'active' : '',
          'round  px-3 py-2 rounded text-black',
        ]"
      >
        <span
          ><svg
            xmlns="http://www.w3.org/2000/svg"
            class="button-icon"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
            aria-label="next button"
            role="img"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M9 5l7 7-7 7"
            ></path></svg
        ></span>
      </button>
    </div>
  </div>
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
const showNextArrow = ref(true);
const showPrevArrow = ref(false);

const nextSlide = () => {
  let slider = document.getElementById("slider");
  let itemWidth = slider.querySelector(".slider-item").offsetWidth + 10;
  slider.scrollBy({
    left: itemWidth * props.itemsPerSlide,
    behavior: "smooth",
  });
  showNextArrow.value = false;
  showPrevArrow.value = true;
};
const prevSlide = () => {
  let slider = document.getElementById("slider");
  let itemWidth = slider.querySelector(".slider-item").offsetWidth + 10;
  slider.scrollBy({
    left: -itemWidth * props.itemsPerSlide,
    behavior: "smooth",
  });
  showPrevArrow.value = false;
  showNextArrow.value = true;
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
  img{
    border-radius: 4px;
  }
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
.controls {
  display: flex;
  height: 100%;
  justify-content: space-between;
  position: absolute;
  width: 100%;
  top: 0;
}
/*
.prevBtn {
  left: 0;
}
.nextBtn {
  right: 0;
}*/
#prevBtn,
#nextBtn {
  color: #fff;
  cursor: pointer;
  height: 100%;
  background: transparent;
  opacity: 0;
}
#nextBtn.active,#prevBtn.active {
  opacity: 1;
}
#nextBtn:hover.active .button-icon,#prevBtn:hover.active .button-icon {
  opacity: 1;
}
.button-icon {
  display: block;
  height: 45px;
  width: 45px;
  color: #fff;
  opacity: 0;
  transition: all 0.3s ease;
}
</style>
