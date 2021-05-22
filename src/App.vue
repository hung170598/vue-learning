<template>
  <div id="app">
    <Header></Header>
    <Body></Body>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from './components/Header'
import Footer from './components/Footer'
import Body from './components/Body'

export default {
  name: "App",
  components: {
    Header,
    Body,
    Footer
  },
  data() {
    return {
      answer: "",
      showCo() {
        this.answer = "Co xinh asdsadsadsa";
      },
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 0;
  background: gray;
}
</style>
