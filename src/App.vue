<template>
  <div id="app">
    <Header />
    <ProfileTop />
    <ProfileBody />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import ProfileTop from './components/profile/ProfileTop.vue'
import ProfileBody from "@/components/profile/profile-body/ProfileBody";

export default {
  name: 'App',
  components: {
    Header,
    ProfileTop,
    ProfileBody,
  }
}
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: 0;
}
</style>
