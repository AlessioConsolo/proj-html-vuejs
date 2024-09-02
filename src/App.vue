<script setup>
import HeaderApp from "./components/HeaderApp.vue";
import MainApp from "./components/MainApp.vue";
import FooterApp from "./components/FooterApp.vue";

const menuItems = [
  {
    href: "/home",
    text: "Home",
    submenu: [
      { href: "#", text: "Submenu 1" },
      { href: "#", text: "Submenu 2" },
    ],
  },
  {
    href: "/pages",
    text: "Pages",
    submenu: [
      { href: "#", text: "Submenu 3" },
      { href: "#", text: "Submenu 4" },
    ],
  },
  {
    href: "/courses",
    text: "Courses",
    submenu: [
      { href: "#", text: "Submenu 5" },
      { href: "#", text: "Submenu 6" },
    ],
  },
  {
    href: "/features",
    text: "Features",
    submenu: [
      { href: "#", text: "Submenu 7" },
      { href: "#", text: "Submenu 8" },
    ],
  },
  {
    href: "/blog",
    text: "Blog",
    submenu: [
      { href: "#", text: "Submenu 9" },
      { href: "#", text: "Submenu 10" },
    ],
  },
  {
    href: "/shop",
    text: "Shop",
    submenu: [
      { href: "#", text: "Submenu 11" },
      { href: "#", text: "Submenu 12" },
    ],
  },
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
