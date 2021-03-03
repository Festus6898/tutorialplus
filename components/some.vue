<template>
  <b-navbar
    class="nav shadow"
    fixed="top"
    toggleable="lg"
    type="light"
    variant="white"
  >
    <b-navbar-brand href="/">
      <b-img
        src="https://storage.googleapis.com/altrekruit_app_assets/website_assets/logo.webp"
        alt="Logo"
        width="155vw"
        fluid
      />
    </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav class="ml-auto mr-5 font-weight-bold">
        <b-nav-item class="custom-nav-item" href="/">Home</b-nav-item>
        <b-nav-item class="custom-nav-item" href="/wipro">Crack Wipro</b-nav-item>
        <b-nav-item class="custom-nav-item" href="/competitive">Competitive Coding</b-nav-item>
        <b-nav-item class="custom-nav-item" href="/entrepreneurship">
          Entrepreneurship
        </b-nav-item>
        <b-nav-item class="custom-nav-item" href="/flutter">
          Flutter Language
        </b-nav-item>
        <b-nav-item class="custom-nav-item" href="/mean">
          MEAN Stack
        </b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script lang="ts">
import { defineComponent } from "@nuxtjs/composition-api";

export default defineComponent({});
</script>

<style scoped>
.navbar-brand {
  padding: 1px;
}
.nav {
  padding-top: 1px;
  padding-bottom: 2px;
}
.nav-btn {
  color: white;
  border: 1px solid #4c00ff00;
  background: linear-gradient(to right, #2f8ce2, #4e42ff);
  border-radius: 50px;
  width: 100%;
}
.nav-btn:hover {
  outline: none;
}

.shadow {
  box-shadow: 0 0.3rem 0.5rem rgba(0, 0, 0, 0.1) !important;
}

@media only screen and (min-width: 992px) {
  .custom-nav-item {
    padding-top: 12px;
    padding-bottom: 9px;
    border-bottom: 3px solid #6b25f600;
  }
  .custom-nav-item:hover {
    border-bottom: 3px solid #6925f6;
  }
  .nav-btn {
    margin-top: 12px;
    margin-bottom: 12px;
  }
}
</style>
