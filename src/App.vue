<template>
  <div class="">
    <navbar-vue />
    <features-vue />
    <mini-bio-vue />
    <testimonies-vue />
    <footer-vue />
  </div>
</template>

<script>
import FeaturesVue from "./components/Features.vue";
import FooterVue from "./components/Footer.vue";
import MiniBioVue from "./components/MiniBio.vue";
import NavbarVue from "./components/Navbar.vue";
import TestimoniesVue from "./components/Testimonies.vue";

export default {
  name: "App",
  components: {
    FeaturesVue,
    MiniBioVue,
    NavbarVue,
    TestimoniesVue,
    FooterVue,
  },
};
</script>

<style></style>
