<template>
  <div id="app">
    <Main/>
  </div>
</template>

<script>
import Main from './components/main'

export default {
  name: 'App',
  components: {
    Main
  }
}
</script>

<style>
#app{
  background: url('//assets-cdn.99plas.com/themes/spring-bg.png') no-repeat center;
  background-size: 100% 100%;
}
</style>
