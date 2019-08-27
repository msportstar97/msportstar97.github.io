<script>
import Main from './components/Main'
import About from './components/About'
import Projects from './components/Projects'
import Contact from './components/Contact'

export default {
  name: 'app',
  components: {
    Main,
    About,
    Projects,
    Contact
  }
}
</script>

<template>
  <div id="app">
    <Main></Main>
    <about></about>
    <projects></projects>
    <contact></contact>
  </div>
</template>

<style>
html {
  scroll-behavior: smooth;
  overflow-x: hidden;
  background-color:#0f5286;
}

body {
  margin: 0px;
  height: 100vh;
  width: 100%;
}

</style>
