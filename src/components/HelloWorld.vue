<template>
  <div class="splash">
    <!-- <Portfolio/> -->
    <Jason/>
  </div>
</template>

<script>
import Portfolio from './textart/portfolio.vue'
import Jason from './textart/jason.vue'
export default {
  name: 'HelloWorld',
  components: {
    Portfolio,
    Jason
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
  justify-content: center;
  align-items: center;
}
</style>
