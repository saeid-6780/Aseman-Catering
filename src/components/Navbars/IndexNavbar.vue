<template>
  <nav
    class="top-0  z-50 w-full flex flex-wrap items-center justify-between px-2 py-3 navbar-expand-lg shadow"
  >
    <div
      class="container px-4 mx-auto flex flex-wrap items-center justify-between"
    >

      <div
        class="flex flex-grow items-center justify-between text-white"
        :class="[navbarOpen ? 'block' : 'hidden']"
        id="example-navbar-warning"
      >
        <div class="mr-auto">
          <button class="">
            <i class="fa fa-phone text-2xl"></i>
          </button>
        </div>
        <div class="m-auto logo-container">
          <img src="@/assets/img/home/logo.png" alt="">
        </div>
        <div class="ml-auto">
          <button class="">
            <i class="fa fa-search text-2xl"></i>
          </button>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>

export default {
  data() {
    return {
      navbarOpen: true,
    };
  },
  methods: {
    setNavbarOpen: function () {
      this.navbarOpen = !this.navbarOpen;
    },
  },

};
</script>
<style>
  .logo-container{max-width: 180px;width: 50%}
</style>
