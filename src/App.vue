<template>
  <Navbar></Navbar>
  <router-view/>

</template>
<script>
import Navbar from "@/components/Navbar.vue"
export default {
  name: '',
  components: {
    Navbar,
  }
}
</script>
<style>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
#app {
  font-family: 'Comfortaa', sans-serif;
  background-color: black;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

</style>
