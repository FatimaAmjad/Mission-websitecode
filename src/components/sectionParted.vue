<template>
    <div class="row">
        <div class="col-6 p-5">
          <slot name="text"/>
        </div>
        <div class="col-6">
          <div class="style-img text-light" :style="{backgroundImage:'url(./img/' + this.link + ')'  ,height:this.leng}"></div>
      </div>
    </div>
</template>
<script>
    export default {
    name: 'sectionParted',
    props: {
    path: String,
    height:Number},
    data(){
        return{
            link:this.path,
            leng:this.height+'px'
        }
    }
}
</script>
<style scoped>
.style-img {
  /* background-image: url(../../public/img/foundation.svg); */
  /* background-image: v-bind(link); */
  background-size: cover;
  background-repeat: no-repeat;
}
</style>