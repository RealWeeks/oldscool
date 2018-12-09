<template>
  <div class="splash">
    <!-- <Portfolio/> -->
    <Jason class="jason-text"/>
    <div class="fake-terminal">
      <div class="line1"><p>Jason@developer-portfolio:</p><VueTinytyper :textSpeed="200" text="Hello..."></VueTinytyper></div>
      
    </div>
    <!-- <VueTinytyper text="Welcome to my portfolio"></VueTinytyper> -->
  </div>
</template>

<script>
import Portfolio from './textart/portfolio.vue'
import Jason from './textart/jason.vue'
import VueTinytyper from 'vue-tinytyper';
export default {
  name: 'HelloWorld',
  components: {
    Portfolio,
    Jason,
    VueTinytyper
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.splash{
  color: green;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.jason-text{
  margin-bottom: 5%;
}
.fake-terminal{
  height: 300px;
  width: 80%;
  background-color: #1e1e23;
  display: flex;
  flex-direction: column;
  font-size: 19px;
}
.line1{
  flex-direction: row;
  display: flex;
}
.line1 p{
  margin-top: 3px;
}
.tiny-typer-container{
  margin-left: 5px;
}
</style>
