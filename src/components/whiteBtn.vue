<template>
    <button type="button" class="btn btn-whi p-2 px-3">{{msg}}</button>
</template>
<script>
    export default {
    name: 'whiteBtn',
    props: {
    msg: String}
}
</script>
<style scoped>
.btn-whi {
  background-color: white;
  color: black;
}
.btn {
  font-size: 10px;
  height: 44px;
  letter-spacing: 2px;
  font-weight: bold;
}
</style>