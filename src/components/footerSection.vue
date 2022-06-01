<template>
<div class="footer py-5">
    <div class="container-fluid">
        <div class="row">
          <div class="col-md-3 col-12 mx-2">
            <img src="img/logo.png" class="logo" />
          </div>
          <div class="col-md-2 col-6 px-md-0 px-4 py-4 sitemap">
            <h6>MISSION DIFFERENCE</h6>
            <ul>
              <li class="my-2">Network</li>
              <li class="my-2">Opportunities</li>
            </ul>
          </div>
          <div class="col-md-2 col-6 px-md-0 px-4 py-4 sitemap">
            <h6>FURTHER READING</h6>
            <ul>
              <li class="my-2">Blog</li>
            </ul>
          </div>
          <div class="col-md-2 col-6 px-md-0 px-4 py-4 sitemap">
            <h6>GET STARTED</h6>
            <ul>
              <li class="my-2">Work with us</li>
              <li class="my-2">Apply to the network</li>
            </ul>
          </div>
        </div>
        <div class="row d-flex flex-md-row flex-column-reverse px-4">
          <div class="col-md-6 col-12 d-flex copyright justify-content-md-start align-items-center justify-content-center">
            2022 All Right Reserved.
          </div>
          <div class="col-md-6 col-12 d-flex justify-content-md-end justify-content-center">
            <img src="img/M-logo.png" style="height: 70px; width: 70px;" />
            <img
              src="img/linkedin-logo.png"
              style="height: 64px; width: 47px;"
            />
          </div>
        </div>
      </div>
</div>
</template>
<script>
export default {
    name:'footerSection',
    data() {
    return {
      primaryBlue: "#3ba3e7",
      primaryPara: "rgb(255,255,255,0.6)",
    };
  },
}
</script>
<style scoped>
.logo {
  height: 64px;
  width: 184px;
}
.sitemap h6 {
  font-size: 10px;
  line-height: 12px;
  color: v-bind(primaryBlue);
  letter-spacing: 2px;
  font-weight: 700;
}
.sitemap ul{
  padding: 0px;
  margin: 0px;
}
.sitemap ul li {
  color: #fff;
  font-size: 16px;
  line-height: 24px;
  text-decoration: none;
  list-style-type: none;
}
.copyright {
  color: v-bind(primaryPara);
  line-height: 24px;
  font-size: 16px;
  font-weight: 400;
  font-style: normal;
}
</style>