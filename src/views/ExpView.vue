<template>
  <div class="about">
    <div class="container">
      <div class="col-md-12 mt-5">
        <h1 class="text_about">Experiences</h1>
      </div>
    </div>
    <div class="container my-5">
      <h2 align="center" class="text_about">My Journey</h2>
      <hr>
      <div v-for="exp in exp_list" class="col-md-12 my-3 jr_exp text-center p-3">
          <img v-bind:src="exp.logo">
          <h3 class="my-2">{{ exp.name }}</h3>
          <p class="my-2">Time: {{ exp.time }}</p>
          <p class="my-2">{{ exp.content }}</p>
        </div>  
    </div>
  </div>
</template>

<script>
export default {
  name: "ExpView",
  data() {
    return {
      exp_list: [
        {
          name: "Study at Vietnam Maritime University",
          time: "10/2020 - Present",
          content: "Major: Information Technology",
          logo: require("@/assets/about/school_logo.png"),
        },
        {
          name: "Intern at VNNET",
          time: "08/2022 - 11/2022",
          content: "Participate in developing water supply management app for smartphone using React Native.",
          logo: require("@/assets/about/vnnet.png"),
        },
        {
          name: "Intern at USI VietNam",
          time: "1/2024 - 4/2024",
          content: "Participate in developing a tools for support MES system for the company.",
          logo: require("@/assets/about/usi.jpg"),
        }
      ],
    };
  },
};
</script>

<style>
.text_about {
  color: #F5F5F5;
  opacity: 1!important;
}

hr {
  border: 1px solid #F5F5F5;
  margin: 1rem 0;
  opacity: .25;
}

.jr_exp{
  background-color: white;
  border-radius: 10px;
}
.jr_exp h3{
  text-decoration: underline;
  font-weight: bold;
}
.jr_exp img{
  width: 200px;
  height: 200px;
}
</style>
