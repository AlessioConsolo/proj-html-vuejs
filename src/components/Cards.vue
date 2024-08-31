<template>
  <div class="card">
    <div class="row">
      <div class="col-4">
        <img :src="getImageUrl(image)" alt="" class="rounded-circle" />
      </div>
      <div class="col-8">
        <h4 class="price-color">
          <strong>{{ price }}</strong>
        </h4>
        <h5>{{ description }}</h5>
        <span class="inline-block ps-3 pe-5">{{ lessons }}</span>
        <span class="inline-block">{{ students }}</span>
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
.card {
  background-color: #fff;
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.rounded-circle {
  border-radius: 50%;
  height: 115px;
  width: 120px;
}

.price-color {
  color: #20ad96;
}
</style>
