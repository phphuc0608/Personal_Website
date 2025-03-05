<template>
  <div class="about">
    <div class="container">
      <div class="col-md-12 mt-5">
        <h1 class="text_about">Experiences</h1>
      </div>
      <hr>
      <div class="description pt-2">
        <div class="col-md-12 des_item text_about mb-2">
          <h3 class="text_about">Key Achievements</h3>
          <ul>
            <li>Selected to participate in a 10 days training course in Kunshan, China. Focusing on data extraction process and CIP project knowledge, management.</li>
            <li>Developed several web applications based on company and client requirements, such as a dashboard aggregation system and an MOI management system.</li>
            <li>Coordinate with departments to implement improvements, saving 15% of costs and ensuring a payback period under one year for automation investments per customer request.</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="container my-5">
      <h2 align="center" class="text_about">My Journey</h2>
      <hr>
      <div v-for="exp in exp_list" :key="exp.name" class="col-md-12 my-3 jr_exp text-center p-3">
        <img :src="exp.logo">
        <h3 class="my-2">{{ exp.name }}</h3>
        <p class="my-2">Time: {{ exp.time }}</p>
        <div class="my-2 text-left">
          <p v-for="(line, index) in exp.content.split('.').filter(Boolean)" :key="index">
            {{ line.trim() }}.
          </p>
        </div>
      </div>  
    </div>
    <div class="container my-5">
      <h2 align="center" class="text_about">My Education</h2>
      <hr>
      <div class="col-md-12 my-3 jr_exp text-center p-3">
        <img src="@/assets/about/school_logo.png">
        <h3 class="my-2">Study at Vietnam Maritime University</h3>
        <p class="my-2">Time: 10/2020 - Present</p>
        <p class="my-2">Major: Information Technology</p>
        <p class="my-2">GPA: 3.28/4.00</p>
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
        // {
        //   name: "Study at Vietnam Maritime University",
        //   time: "10/2020 - Present",
        //   content: "Major: Information Technology",
        //   logo: require("@/assets/about/school_logo.png"),
        // },
        {
          name: "Smart Manufacturing Development Engineer at USI VietNam",
          time: "7/2024 - Present",
          content: "Managed CIP projects to optimize quality, output, and cycle times through team collaboration. Facilitated communication between engineering teams and clients for project success. Developed digitalization software to meet company and client-specific needs.",
          logo: require("@/assets/about/usi.jpg"),
        },
        {
          name: "IT internship at USI VietNam",
          time: "1/2024 - 4/2024",
          content: "Participate in developing a tools for support MES system for the company. Learned about MES operating and production management systems. Assisted in enhancing efficiency and productivity within the team.",
          logo: require("@/assets/about/usi.jpg"),
        },
        {
          name: "IT internship at VNNET",
          time: "08/2022 - 11/2022",
          content: "Participate in developing water supply management app for smartphone using React Native.",
          logo: require("@/assets/about/vnnet.png"),
        },
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
