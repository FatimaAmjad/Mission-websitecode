<template>
    <div class="message-item p-4">
                <p>
                  <slot></slot>
                </p>
                <div class="sender my-4">
                  <h6 class="name mb-1">{{name}}</h6>
                  <h6 class="role">{{role}}</h6>
                </div>
              </div>
</template>
<script>
    export default {
    name: 'messageItem',
    props: {
    name: String,
    role:String},
    data() {
    return {
      primaryPink: "#e64b91",
      primaryPara: "rgb(255,255,255,0.6)",
    };
  },
}
</script>
<style scoped>
.message-item {
  border: 1px solid rgba(255, 255, 255, 0.2);
  box-sizing: border-box;
  border-radius: 12px;
  height: 658px;
}
.message-item p {
  font-weight: 400;
  font-style: normal;
  font-size: 20px;
  line-height: 32px;
  color: v-bind(primaryPara);
  text-align: left;
}
.sender {
  text-align: left;
}
.sender .name {
  color: v-bind(primaryPink);
  font-size: 16px;
  line-height: 20px;
  font-weight: 700;
  letter-spacing: 2px;
}
.sender .role {
  font-weight: 400;
  font-style: normal;
  font-size: 16px;
  line-height: 24px;
  color: v-bind(primaryPara);
}
@media screen and (max-width: 1200px){
p{
    font-size: 16px!important;
    line-height: 24px!important;
}
.message-item{
  height: 515px;
}
}
</style>