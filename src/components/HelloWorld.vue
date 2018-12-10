<template>
  <div class="splash">
    <Jason class="jason-text"/>
    <h4 @click="handleBale">Bale here</h4>
    <div class="fake-terminal">
      <div class="line1"><p>Jason@developer-portfolio:</p><VueTinytyper
        :textSpeed="75"
        text="Hello... Welcome to my portfolio"
        @animation-finished="line1Done = true"
        :staticCursor="!line1Done"
        :cursor="';'"
        ></VueTinytyper>
      </div>

      <div v-if="line1Done" class="line1"><p>Jason@developer-portfolio:</p><VueTinytyper
        :textSpeed="75"
        text="Your cursor has been disabled. Please your your keyboard"
        @animation-finished="line2Done = true"
        :staticCursor="!line2Done"
        :cursor="';'"
        ></VueTinytyper>
      </div>

      <div v-if="line2Done" class="line1"><p>Jason@developer-portfolio:</p><VueTinytyper
        :textSpeed="75"
        text="Let me get you started"
        @animation-finished="line3Done = true"
        :cursor="';'"
        :staticCursor="!line3Done"
        ></VueTinytyper>
      </div>

      <div v-if="line3Done" class="line1"><p>Jason@developer-portfolio:</p><VueTinytyper
        :textSpeed="75"
        text="/help"
        @animation-finished="line4Done = true"
        :cursor="';'"
        :staticCursor="!line4Done"
        ></VueTinytyper>
      </div>

      <div class="commands" v-if="line4Done">
        <div>Commands:</div>
        <div>Projects               view personal projects created by me</div>
        <div>Github                 view my github page</div>
        <div>Linkedin               view my linked page</div>
        <div>Resume                 view my resume</div>
      </div>

    </div>

     <div v-if="line4Done" class=term-text-wrapper>
        <input ref="termInput" @keyup.enter="handleSearch" v-model="searchText" class="term-input-txt" type="text" placeholder="Type here. Press enter to submit.">
      </div>
  </div>
</template>

<script>
import Jason from './textart/jason.vue'
import VueTinytyper from 'vue-tinytyper'
export default {
  name: 'HelloWorld',
  components: {
    Jason,
    VueTinytyper
  },
  props: {
    msg: String
  },
  methods: {
    handleSearch () {
      let search = this.searchText
      if (search.toLowerCase().includes('help')) {
        // this.handleHelp()
      } else if (search.toLowerCase().includes('projects')) {

      }
    },
    handleBale () {
      debugger
      this.$router.push({ path: 'standard' })
    }
    // handleHelp() {

    // }
  },
  watch: {
    line4Done () {
      if (this.line4Done) {
        this.$nextTick(() => this.$refs.termInput.focus())
      }
    }
  },
  data: function () {
    return {
      line1Done: false,
      line2Done: false,
      line3Done: false,
      line4Done: false,
      searchText: 'Guest@developer-portfolio: '
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* @import url('https://fonts.googleapis.com/css?family=VT323'); */
@import url('https://fonts.googleapis.com/css?family=Roboto+Mono');
.splash{
  color: green;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: black;
}
.jason-text{
  margin-bottom: 5%;
}
.fake-terminal{
  /* font-family: 'VT323', monospace; */
  font-family: 'Roboto Mono', monospace;
  height: 400px;
  width: 80%;
  background-color: #1e1e23;
  display: flex;
  flex-direction: column;
  font-size: 19px;
}
.line1{
  flex-direction: row;
  display: flex;
  margin-bottom: 0px;
}
.line1 p{
  margin-top: 1px;
}
.tiny-typer-container{
  margin-left: 5px;
}
.commands{
  /* font-family: 'VT323', monospace; */
  font-family: 'Roboto Mono', monospace;
  display: flex;
  flex-direction: column;
  white-space: pre;
}
.commands div:not(:first-child) {
  margin-left: 15px;
}
.term-input-txt{
  width: 100%;
  color: green;
  border-right-width: 0px;
  padding-right: 0px;
  background-color: #1e1e22;
  border: 0;
  height: 100%;
  padding: 0;
  font-size: medium;
  font-family: 'Roboto Mono', monospace;
}
.term-text-wrapper{
  /* font-family: 'VT323', monospace; */
  width: 80%;
  height: 18px;
}
::placeholder { /* Chrome, Firefox, Opera, Safari 10.1+ */
  color:green;
  opacity: 1; /* Firefox */
}
</style>
