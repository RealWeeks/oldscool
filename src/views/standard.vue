<template>
  <div class="standard">
    <div class="img-wrapper">
      <img class="image-back" src="../assets/code-screen.jpg">
      <div class="centered">Hey, I'm Jason.</div>
      <div class="centered-below">Thanks for visiting my portfolo.</div>
      
    </div>
      <!-- <md-button >Default</md-button> -->
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
.centered-below{
  position: absolute;
  top: 54%;
  left: 54%;
  transform: translate(-50%, -50%);
  color: white;
  font-size: 6em;
}
.centered{
  position: absolute;
  top: 37%;
  left: 45%;
  transform: translate(-50%, -50%);
  color: white;
  font-size: 8em;
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
