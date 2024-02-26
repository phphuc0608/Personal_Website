<template>
  <div class="about">
    <div class="container">
      <div class="col-md-12 mt-5">
        <h1 class="text_about">About</h1>
      </div>
      <div class="col-md-6 text_about mb-4">
        Hello, I'm Pham Quang Phuc, but you can simply call me Mac. I am a programmer.
      </div>
      <!-- <div class="col-md-6 text_about" style="font-size: 13px;">
        I'm currently a student at the University of Information Technology, majoring in Software Engineering.
        I'm also a self-taught web developer, and I'm always looking for new things to learn. 
      </div> -->
    </div>
    <div class="container my-5">
      <h2 align="center" class="text_about">My Journey</h2>
      <hr>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutView",
  data() {
    return {
    };
  },
};
</script>

<style>
.text_about {
  color: #F5F5F5;
  opacity: 1 !important;
}

hr {
  border: 1px solid #F5F5F5;
  margin: 1rem 0;
  opacity: .25;
}

.jr_exp {
  background-color: white;
  border-radius: 10px;
}

.jr_exp h3 {
  text-decoration: underline;
  font-weight: bold;
}

.jr_exp img {
  width: 200px;
  height: 200px;
}
</style>
