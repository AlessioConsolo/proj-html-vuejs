<template>
  <div class="container-fluid main-bg">
    <div class="container py-5">
      <div class="col">
        <div class="footer d-flex justify-content-between">
          <div class="address">
            <h5>Address</h5>
            <ul>
              <li
                class="sub-gray"
                v-for="(item, index) in address"
                :key="index"
              >
                {{ item.text }}
              </li>
            </ul>
            <div class="socials">
              <a href="#"
                ><i
                  class="fa-brands fa-square-facebook fa-lg me-3"
                  style="color: #b7b7b7"
                ></i
              ></a>
              <a href="#"
                ><i
                  class="fa-brands fa-twitter fa-lg me-3"
                  style="color: #b7b7b7"
                ></i
              ></a>

              <a href="#"
                ><i
                  class="fa-brands fa-instagram fa-lg me-3"
                  style="color: #b7b7b7"
                ></i
              ></a>

              <a href="#"
                ><i
                  class="fa-brands fa-linkedin fa-lg"
                  style="color: #b7b7b7"
                ></i
              ></a>
            </div>
          </div>
          <div class="info-links gap-5 d-flex">
            <div class="explore">
              <h5>Explore</h5>
              <ul>
                <li v-for="(item, index) in explore" :key="index">
                  <a :href="item.link">{{ item.text }}</a>
                </li>
              </ul>
            </div>
            <div class="unknown">
              <ul>
                <li v-for="(item, index) in unknown" :key="index">
                  <a :href="item.link">{{ item.text }}</a>
                </li>
              </ul>
            </div>
            <div class="information">
              <h5>Information</h5>
              <ul>
                <li v-for="(item, index) in information" :key="index">
                  <a :href="item.link">{{ item.text }}</a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col text-center">
          <p class="sub-gray">2020 MaxCoach. All Rights Reserved</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    address: Array,
    explore: Array,
    information: Array,
    unknown: Array,
  },
};
</script>
<style lang="scss" scoped>
@import "../generals.scss";

ul {
  list-style: none;
}

li {
  margin-left: -32px;
  line-height: 2.5rem;
}

a {
  text-decoration: none;
  color: $sub-color-gray;
}

.unknown li {
  line-height: 2.5rem;
}

.unknown ul {
  margin-top: 31px;
}

.sub-gray {
  color: $sub-color-gray;
}

a:hover {
  color: $green-main;
}

i:hover {
  color: $green-main !important;
}
</style>
