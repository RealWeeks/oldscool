<template>
  <div class="project">
    test
  </div>
</template>

<script>
import VueTinytyper from 'vue-tinytyper';
export default {
  name: 'Standard',
  components: {
    VueTinytyper
  },
  props: {
  },
  methods: {
  },
  watch: {
  },
  data: function () {
  return {

  }
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');
.standard{
  font-family: 'Source Sans Pro', sans-serif;
}
.md-button{
  color: white !important;
  background-color: gray !important;
}
.bottom-left{
  position: absolute;
  top: 72%;
  left: 72%;
  transform: translate(-50%, -50%);
  color: white;
  font-size: 5vw;
}
.centered-below{
  position: absolute;
  top: 54%;
  left: 54%;
  transform: translate(-50%, -50%);
  color: white;
  font-size: 5vw;
}
.centered{
  position: absolute;
  top: 37%;
  left: 49%;
  transform: translate(-50%, -50%);
  color: white;
  font-size: 13vw;
}
.img-wrapper{
  position: fixed;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
}
.image-back{
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  margin: auto;
  min-width: 50%;
  min-height: 50%;
}
</style>
