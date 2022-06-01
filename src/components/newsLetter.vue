<template>
<div class="news-letter py-5">
    <div class="news container p-lg-5 p-3">
        <h3 class="my-1">News and Updates</h3>
        <p class="my-4">
          Subscribe to our newsletter to stay up to date on the latest
          developments coming to Mission.
        </p>
        <div class="d-flex justify-content-center my-4">
          <div class="email-bar d-flex">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              fill="currentColor"
              class="bi bi-envelope"
              viewBox="0 0 16 16"
            >
              <path
                d="M0 4a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V4Zm2-1a1 1 0 0 0-1 1v.217l7 4.2 7-4.2V4a1 1 0 0 0-1-1H2Zm13 2.383-4.708 2.825L15 11.105V5.383Zm-.034 6.876-5.64-3.471L8 9.583l-1.326-.795-5.64 3.47A1 1 0 0 0 2 13h12a1 1 0 0 0 .966-.741ZM1 11.105l4.708-2.897L1 5.383v5.722Z"
              />
            </svg>
            <input
              id="email-address"
              type="email"
              name="email"
              class="form-control"
              placeholder="Your email"
              required=""
            />
            <bluebtn msg="SUBSCRIBE"/>
          </div>
        </div>
      </div>
</div>
</template>
<script>
import bluebtn from './bluebtn.vue';
    export default {
  components: { bluebtn },
    name: 'newsLetter',
    data() {
    return {
        primaryPara: "rgb(255,255,255,0.6)",
        primaryNavLight: "#27263a",
    };
  },
}
</script>
<style scoped>
.news-letter {
  background: v-bind(primaryNavLight);
  text-align: center;
}
.news h3 {
  font-weight: 400;
  font-size: 40px;
  line-height: 56px;
  color: #fff;
  text-align: center;
  letter-spacing: 2px;
}
.news p {
  font-weight: 400;
  text-align: center;
  color: v-bind(primaryPara);
  font-style: normal;
  line-height: 32px;
  font-size: 20px;
}
.email-bar {
  position: relative;
  display: inline;
  font-size: 1rem;
  color: white;
  background-color: #535269;
  align-items: center;
  padding-left: 20px;
  border-radius: 8px;
  width: 40%;
}
.form-control {
  color: white;
  background-color: #535269;
  font-weight: 400;
  font-size: 16px;
  color: v-bind(primaryPara);
  border: 0;
  outline: 0;
  border-radius: 8px 0 0 8px;
}
svg {
  color: #949aa0;
}
.email-bar button {
  border-radius: 0px 8px 8px 0px;
}
@media screen and (max-width: 1200px){

.email-bar{
  width: 60%!important;
}
.email-bar svg{
  height: 32px!important;
  width: 32px!important;
}
}
@media screen and (max-width: 480px){
    h3{
        font-size: 24px!important;
    line-height: 32px!important;
    }
    .email-bar{
  width: 70%!important;
}
}
</style>