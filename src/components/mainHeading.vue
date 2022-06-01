<template>
    <h3 :style="{color:col}">
        <slot></slot>
    </h3>
</template>
<script>
export default {
    name:'mainHeading',
    props:{
        col:String
    }
}
</script>
<style scoped>
h3 {
  font-weight: 100;
  font-style: normal;
  line-height: 56px;
  font-size: 40px;
  letter-spacing: 2px;
}
@media screen and (max-width: 1200px){
h3{
    font-size: 36px!important;
    line-height: 48px!important;
    font-weight: 300;
}}
@media screen and (max-width: 480px){
    h3{
        font-size: 24px!important;
    line-height: 32px!important;
    }
}
</style>