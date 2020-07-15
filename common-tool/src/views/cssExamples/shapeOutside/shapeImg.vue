<template>
  <div class="shapes"></div>
</template>

<script>
export default {
  name: "shapeImg"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.shapes {
  width: 150px;
  height: 150px;
  float: left;
  padding: 10px;
  margin: 10px;
  border-radius: 50%;
  border: 10px solid #2d8cf0;
  background-image: linear-gradient(30deg, #2d8cf0, transparent 80%, transparent);
}
</style>
