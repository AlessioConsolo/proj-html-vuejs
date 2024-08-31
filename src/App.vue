<script setup>
import HeaderApp from "./components/HeaderApp.vue";
import MainApp from "./components/MainApp.vue";
import FooterApp from "./components/FooterApp.vue";

const menuItems = [
  { href: "/home", text: "Home" },
  { href: "/pages", text: "Pages" },
  { href: "/courses", text: "Courses" },
  { href: "/features", text: "Features" },
  { href: "/blog", text: "Blog" },
  { href: "/shop", text: "Shop" },
];
</script>

<template>
  <HeaderApp :menuItems="menuItems" />
  <MainApp />
  <FooterApp />
</template>

<style scoped></style>
