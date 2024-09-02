<template>
  <div class="slider my-5">
    <div
      v-for="(slide, index) in slides"
      :key="index"
      class="main-white p-3 mx-3"
    >
      <p class="fw-600 main-purple">{{ slide.title }}</p>
      <p class="sub-gray">{{ slide.description }}</p>
      <img
        :src="getImageUrl(slide.image)"
        alt=""
        :key="index"
        class="rounded-circle float-start"
      />
      <span class="main-purple fw-600 info-img">{{ slide.name }}</span>
      <p class="sub-gray info-p">{{ slide.job }}</p>
    </div>
  </div>
  <div class="dots mb-5">
    <span
      v-for="(dot, index) in slides"
      :key="index"
      @click="setCurrentSlide(index)"
      :class="{ active: currentIndex === index }"
    ></span>
  </div>
</template>

<script>
export default {
  props: {
    slides: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      currentIndex: 0,
    };
  },
  methods: {
    setCurrentSlide(index) {
      this.currentIndex = index;
    },
    getImageUrl(image) {
      return new URL(`../assets/${image}`, import.meta.url).href;
    },
  },
};
</script>

<style>
.dots span {
  display: inline-block;
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background-color: #ccc;
  margin: 0 5px;
  cursor: pointer;
}

.dots span.active {
  background-color: #333;
}

.slider {
  overflow-x: hidden;
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.slider > div {
  width: 100%;
  position: relative;
  transition: transform 0.5s ease-in-out;
}

.dots {
  text-align: center;
  margin-top: 20px;
  justify-content: center;
  display: flex;
  justify-content: center;
}

.info-img {
  margin-top: 30px;
  display: inline-block;
  margin-left: 20px;
}

.info-p {
  padding-left: 80px;
}

.rounded-circle {
  height: 60px;
  width: 60px;
  margin-top: 15px;
}
</style>
