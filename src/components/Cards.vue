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
        <h5 class="fw-600 desc">{{ description }}</h5>
        <span class="inline-block sub-gray pe-5"
          ><i class="fa-solid fa-file-lines"></i> {{ lessons }}</span
        >
        <span class="inline-block sub-gray"
          ><i class="fa-regular fa-user"></i> {{ students }}</span
        >
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
  float: inline-end;
}

.price-color {
  color: $green-main;
}

.desc:hover {
  color: $green-main;
  cursor: pointer;
}
</style>
