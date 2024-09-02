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

const address = [
  { text: "382 NE 191st St # 87394 Miami, FL 33179-3899" },
  { text: "+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)" },
  { text: "support@maxcoach.com" },
];

const explore = [
  { link: "#", text: "Start here" },
  { link: "#", text: "Blog" },
  { link: "#", text: "About us" },
];

const unknown = [
  { link: "#", text: "Success story" },
  { link: "#", text: "Courses" },
  { link: "#", text: "Contact us" },
];

const information = [
  { link: "#", text: "Membership" },
  { link: "#", text: "Purchase guide" },
  { link: "#", text: "Privacy policy" },
  { link: "#", text: "Terms of services" },
];
</script>

<template>
  <HeaderApp :menuItems="menuItems" />
  <MainApp />
  <FooterApp
    :address="address"
    :explore="explore"
    :information="information"
    :unknown="unknown"
  />
</template>

<style scoped></style>
