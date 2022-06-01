<template>
    <div class="d-block">
        <div class="container-fluid">
          <div
            class="row nav-fixed py-2 px-3 w-100"
            :class="{ onScroll: !view.topOfPage }"
          >
            <div class="col-3  d-lg-none d-flex align-items-center">
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" class="bi bi-list text-light" viewBox="0 0 16 16">
                <path fill-rule="evenodd" d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"/>
              </svg>
            </div>
            <div class="col-lg-3 col-6 d-flex justify-content-lg-start align-items-center justify-content-center">
              <img src="img/logo.png" class="logo" />
            </div>
            <div class="col-6 d-lg-flex d-none nav-links justify-content-center align-items-center">
              <ul>
                <li class="mx-3">NETWORK</li>
                <li class="mx-3">OPPORTUNITIES</li>
              </ul>
            </div>
            <div class="col-3 nav-links d-flex justify-content-end align-items-center">
              <ul>
                <li class="mx-3">LOGIN</li>
                <li class="d-lg-inline d-none">
                  <Bluebtn msg="APPLY NOW"/>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
</template>
<script>
import Bluebtn from './bluebtn.vue';
export default {
    name:'navBar',
    components:{
        Bluebtn
  },
  data() {
    return {
      view: {
        topOfPage: true,
      },
      primaryBlue: "#3ba3e7",
      primaryOrange: "#ff7e75",
      primaryPink: "#e64b91",
      primaryNav: "#222238",
      primaryPara: "rgb(255,255,255,0.6)",
      primaryBg: "#0b0a1a",
      primaryNavLight: "#27263a",
    };
  },
  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      var scroll = window.scrollY;
      if (scroll > 100) {
        if (this.view.topOfPage) this.view.topOfPage = false;
      } else {
        if (!this.view.topOfPage) this.view.topOfPage = true;
      }
    },
  },
};
</script>
<style scoped>
.nav-fixed {
  background-color: transparent;
  height: 80 !important;
  font-size: 10px;
  font-weight: bold;
  letter-spacing: 2px;
  z-index: 10;
  transition: background-color 0.2s ease-in-out;
  position: fixed;
  top: 0;
}
.nav-links ul {
  margin-top: 0px !important;
  margin-bottom: 0px !important;
}
.nav-links ul li {
  text-decoration: none;
  display: inline;
  color: white;
}
.logo {
  height: 64px;
  width: 184px;
}
.onScroll {
  background-color: v-bind(primaryNav);
}

</style>