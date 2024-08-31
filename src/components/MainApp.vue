<template lang="html">
  <div class="container">
    <div class="row my-5">
      <div class="col-6">
        <h2>Distant learning for further expansion</h2>
        <p>
          Learning is a life-long journey that in fact we never find the
          terminate stop. Stop searching, enjoy the process.
        </p>
        <button type="button">Download free guide</button>
        <p>Have questions? <a href="#">Get Free Sample -></a></p>
      </div>
      <div class="col-6">
        <img
          src="../assets/about-me-profile-ohm4dxoearqbxny7q3bq1pzbdgofdx0tobbeqcvzd0.jpg"
          alt=""
          class="rounded-circle w-100 h-100"
        />
      </div>
      <div class="col">
        <div
          class="partners d-flex justify-content-between align-items-center my-5"
        >
          <img class="img-fluid" src="../assets/client-logo-01.png" alt="" />
          <img class="img-fluid" src="../assets/client-logo-02.png" alt="" />
          <img class="img-fluid" src="../assets/client-logo-03.png" alt="" />
          <img class="img-fluid" src="../assets/client-logo-04.png" alt="" />
          <img class="img-fluid" src="../assets/client-logo-05.png" alt="" />
          <img class="img-fluid" src="../assets/client-logo-06.png" alt="" />
        </div>
      </div>
    </div>
  </div>
  <div class="container-fluid main-bg">
    <div class="container">
      <div class="row pt-5">
        <div class="col mb-5 text-center">
          <p>STIMULATED TO LEARN?</p>
          <h2>Featured Online Courses</h2>
        </div>
      </div>
      <div class="cards d-flex gap-5 flex-wrap justify-content-center">
        <Card
          class="width-40"
          image="course-02-480x298.jpg"
          price="€40,00"
          description="Learning to Write as a Professional Author"
          lessons="20 Lessons"
          students="50 Students"
        />
        <Card
          class="width-40"
          image="stock-full-hd-03-480x298.jpg"
          price="€19,00"
          description="Open Programming Courses for Everyone: Python"
          lessons="17 Lessons"
          students="62 Students"
        />
        <Card
          class="width-40"
          image="stock-full-hd-04-480x298.jpg"
          price="€39,00"
          description="Master jQuery in a Short Period of Time"
          lessons="6 Lessons"
          students="51 Students"
        />
        <Card
          class="width-40"
          image="stock-full-hd-06-480x298.jpg"
          price="Free"
          description="Customer-centric Info-Tech Strategies"
          lessons="24 Lessons"
          students="769 Students"
        />
        <Card
          class="width-40"
          image="course-featured-image-01-480x298.jpg"
          price="€26,00"
          description="Academic Listening and Note-taking"
          lessons="14 Lessons"
          students="67 Students"
        />
        <Card
          class="width-40"
          image="stock-full-hd-05-480x298.jpg"
          price="€59,00"
          description="Introduction to Javascript For Beginners"
          lessons="14 Lessons"
          students="76 Students"
        />
      </div>
    </div>
  </div>
</template>
<script>
import Card from "./Cards.vue";

export default {
  components: { Card },
};
</script>
<style lang="scss">
@import "../generals.scss";

.partners {
  img {
    width: fit-content;
    height: fit-content;
  }
}
.cards {
  .width-40 {
    width: 40%;
  }
}

.main-bg {
  background-color: $bg-color-gray;
}
</style>
