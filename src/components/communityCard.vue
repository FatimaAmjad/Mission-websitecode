<template>
    <div
        class="card d-flex flex-column p-3 px-4"
        :style="{backgroundColor:this.color}"
    >
        <img
        :src="require(`../../public/img/${this.path}.png`)"
        :style="{height: this.height+'px', width:this.width+'px' }"
        />
        <div class="card-text mt-4">
        <h3>{{name}}</h3>
        <p class="my-2 mt-3">
            <slot></slot>
        </p>
        </div>
    </div>
</template>
<script>
export default {
    name: 'communityCard',
    props: {
        color: String,
        height:Number,
        width:Number,
        path:String,
        name: String
        },
    data(){
        return{
            img:"./img/"+this.path,
            primaryPara: "rgb(255,255,255,0.6)",
        }
    }
}
</script>
<style scoped>
.card{
    border-radius: 8px;
    height: 365px;
    transition: .3s transform cubic-bezier(.155,1.105,.295,1.12),.3s box-shadow,.3s -webkit-transform cubic-bezier(.155,1.105,.295,1.12);
}
.card-text h3 {
  font-weight: 600;
  font-style: normal;
  font-size: 24px;
  line-height: 32px;
  color: #fff;
}
.card-text p {
  font-weight: 400;
  font-style: normal;
  font-size: 16px;
  line-height: 24px;
  color: v-bind(primaryPara);
}
.card:hover{
     transform: scale(1.05);
    box-shadow: 0 10px 20px rgba(0,0,0,.12), 0 4px 8px rgba(0,0,0,.06);
}
@media screen and (max-width: 1200px){
    .card{
    border-radius: 8px;
    height: 270px;
}
}
</style>