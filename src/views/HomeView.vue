<template>
  <!-- Main Content -->
  <div class="container mt-5 main_content d-flex justify-content-center">
    <div class="row">
      <div class="col-md-12 text-center d-flex align-items-center justify-content-center">
        <img src="../assets/avatar.jpg" class="img-fluid rounded-circle" width="250" height="250">
      </div>
      <div id="greeting" class="col-md-12 text-light d-flex justify-content-center">
        <span class="text-center">Welcome to my portfolio</span>
      </div>
      <div id="social_container" class="col-md-12 d-flex justify-content-center" style="color: white">
        <a class="p-3" href="https://github.com/phphuc0608" target="_blank"><i class="bi bi-github contact_icon"></i></a>
        <a class="p-3" href="https://www.facebook.com/pham.phuc.5815255" target="_blank"><i class="bi bi-facebook contact_icon"></i></a>
        <a class="p-3" href="https://www.linkedin.com/in/ph%E1%BA%A1m-quang-ph%C3%BAc-492524298/" target="_blank"><i class="bi bi-linkedin contact_icon"></i></a>
      </div>
    </div>
  </div>
  <Footer></Footer>
</template>


<script>
// @ is an alias to /src
import Footer from "@/components/Footer.vue"

export default {
  name: '',
  components: {
    Footer,
  }
}
</script>

<style scoped>
.main_content {
  flex: 1;
}
#social_container {
  float: left;
  flex-direction: row;
}
#social_container i{
  font-size: 60px;
}
#social_container a {
  text-decoration: none;
  color: white;
}
#greeting span{
  font-size: 25pt;
  text-transform: uppercase;
  font-weight: bold;
  padding: 30px 0px;
}
.contact_icon:hover {
  cursor: pointer;
  color: hsla(0,0%,100%,.75);
}
@media (max-width: 358px) {
  #greeting span{
    font-size: 20pt;
    padding: 30px 0px;
}
}
</style>
