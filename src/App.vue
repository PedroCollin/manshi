<template>
  <div id="app_div">
    <Navbar text_color="white" back_color="#080404" img_logo="/images/ramen.svg"/>
    <router-view />
  </div>
</template>

<script>

  import Navbar from './components/Navbar.vue'

  export default {
    name: 'App',
    components: {
      Navbar
    }
  }
</script>


<style src="./App.css">

</style>
