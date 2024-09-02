<template>
  <div class="card-custom">
    <div class="row">
      <div class="col-4">
        <img :src="getImageUrl(image)" alt="" class="rounded-circle" />
      </div>
      <div class="col-8">
        <h4 class="price-color">
          <strong>{{ price }}</strong>
        </h4>
        <h5 class="fw-600">{{ description }}</h5>
        <span class="inline-block sub-gray ps-3 pe-5">{{ lessons }}</span>
        <span class="inline-block sub-gray">{{ students }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    image: String,
    lessons: String,
    students: String,
    description: String,
    price: String,
  },
  methods: {
    getImageUrl(image) {
      return new URL(`../assets/${image}`, import.meta.url).href;
    },
  },
};
</script>

<style lang="scss">
@import "../generals.scss";

.card-custom {
  background-color: $bg-color-gray;
  padding: 20px;
}

.rounded-circle {
  border-radius: 50%;
  height: 115px;
  width: 120px;
}

.price-color {
  color: $green-main;
}
</style>
