<template>
    <button type="button" class="btn btn-pri p-2 px-3">{{msg}}</button>
</template>
<script>
    export default {
    name: 'blueBtn',
    props: {
    msg: String},
    data() {
    return {
      primaryBlue: "#3ba3e7",
    };
  },
}
</script>
<style scoped>
.btn-pri {
  background-color: v-bind(primaryBlue);
  color: white;
}
.btn {
  font-size: 10px;
  height: 44px;
  letter-spacing: 2px;
  font-weight: bold;
}
.btn:hover{
  color: white;
}
</style>