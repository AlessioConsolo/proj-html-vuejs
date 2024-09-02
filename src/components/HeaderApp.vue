<template lang="html">
  <div class="container">
    <div class="row pb-5">
      <div class="col d-flex my-4 align-items-center justify-content-between">
        <div class="logo">
          <img class="max-w-60" src="../assets/dark-logo.png" alt="Logo" />
        </div>
        <div class="menu d-flex">
          <ul class="d-flex gap-5 mx-5">
            <li
              v-for="(item, index) in menuItems"
              :key="index"
              class="dropdown"
            >
              <a
                href="#"
                class="dropdown-toggle"
                data-bs-toggle="dropdown"
                aria-expanded="false"
                role="button"
                @click.prevent
              >
                {{ item.text }}
              </a>
              <ul class="dropdown-menu">
                <li
                  v-for="(submenuItem, submenuIndex) in item.submenu"
                  :key="submenuIndex"
                >
                  <a :href="submenuItem.href">{{ submenuItem.text }}</a>
                </li>
              </ul>
            </li>
          </ul>
          <div class="searchbar">
            <input
              class="form-control mr-sm-2"
              type="search"
              placeholder="Search"
              aria-label="Search"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
import { defineProps } from "vue";

defineProps({
  menuItems: {
    type: Array,
    required: true,
  },
});
</script>
<style lang="scss">
@import "../generals.scss";

.menu {
  ul {
    list-style: none;
  }

  a {
    text-decoration: none;
    color: #696969;
  }
}

.max-w-60 {
  max-width: 60%;
}
</style>
