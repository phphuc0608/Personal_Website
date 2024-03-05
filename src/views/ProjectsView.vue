<template>
<div class="container ">
  <div class="col-md-12 mt-5">
    <h1 class="text_about">Projects</h1>
  </div>
  <div class="pt-2">
    <div class="col-md-6 text_about mb-2">
      Of course, I can't call myself a tech guy without some software projects.
    </div>
  </div>
  <hr>
  <div id="project_container" v-for="project in projects">
    <div class="col-md-12 project_box">
      <div class="col-lg-5 col-md-12 me-lg-4">
        <h3 class="text_about">{{ project.name }}</h3>
        <span class="text_about justified_text">
          {{ project.content }}
        </span>
        <br>
        <div class="tech_container mt-3">
          <span v-for="tech_item in project.tech" class="mx-1 my-1 p-2 tech_item">{{ tech_item }}</span>
        </div>
        <div class="mt-4">
          <span class="github p-2">
            <i class="fa-brands fa-github me-2"></i> 
            <a :href="project.github" target="_blank" class="text_about">Link to github</a>
          </span>
        </div>
      </div>
      <div class="col-lg-7 col-md-12">
        <img :src="project.img" class="img_pro" alt="">
      </div>
    </div>
    <hr>
  </div>
</div>
</template>

<script>
export default {
  data(){
    return{
      projects: [
        {
          name: "Website selling technology items PHP version",
          content: "The goal of this project is to create a management page and a sales page. The management page helps user manage products, accounts, product types, manufacturers and news available on the website. The sales page will display the products, product types and news currently in the database.",
          img: require("@/assets/projects/project_php.png"),
          tech: ["PHP", "HTML", "CSS", "MySQL", "Bootstrap", "Jquery"],
          github: "https://github.com/phphuc0608/Web_Selling_Phones_v1",
        },
        {
          name: "Website selling technology items Laravel version",
          content: "The goal of this project is to create a management page and a sales page. The management page helps user manage products, accounts, product types, manufacturers and news available on the website.",
          img: require("@/assets/projects/project_laravel.png"),
          tech: ["Laravel", "HTML", "CSS", "MySQL", "Bootstrap", "JavaScript"],
          github: "https://github.com/phphuc0608/Web_Selling_Phones_v2",
        },
        {
          name: "Emotion recognition",
          content: "This project's content is to create a model that can recognize 7 types of human emotions through the face. The project includes two simple apps: recognition through images and recognition with cameras in real time.",
          img: require("@/assets/projects/project_emotion.png"),
          tech: ["Python", "OpenCV", "Numpy", "Keras", "Pandas"],
          github:"https://github.com/phphuc0608/Emotion-recognition",
        },
        {
          name: "League of legends skins store and items",
          content: "This is a website that simulates buying and selling items and costumes for champions in League of Legends, where users can easily search, view and buy costumes for their characters.",
          img: require("@/assets/projects/project_lol.png"),
          tech: ["Laravel", "HTML", "CSS", "MySQL", "Bootstrap", "JavaScript"],
          github:"https://github.com/phphuc0608/LoL_shop"
        },
        {
          name: "Test automation platform for web API",
          content: "This software was created for do test web API and generate report automatically. It will have 3 parts: manual test, auto test and flexible test. Manual testing allows users to test manually with the scenarios they want. The auto test part will have pre-built scenarios to conduct testing. Finally, the flexible test part will allow users to create their own test scenarios and input the API they want.",
          img: require("@/assets/projects/project_usi.png"),
          tech:["VueJS","HTML","CSS", "Bootstrap", "JavaScript"],
          github:"https://github.com/phphuc0608/MES_WEB_API_Test_Platform_USI",
        }
      ]
    }
  },
}
</script>

<style scoped>
.img_pro {
  width: 100%;
  border-radius: 10px;
}
.justified_text {
  text-align: justify;
}
.tech_container{
  display: flex;
  flex-wrap: wrap;
}
.tech_item{
  background-color: azure;
  border-radius: 10px;
}
.github{
  margin-top: 10px;
  background-color: rgb(54, 54, 54);
  color: white;
  border-radius: 10px;
  transition: 0.5s;
  text-decoration: none;
}
.github:hover{
  border: 1px solid white;
  cursor: pointer;
}
.project_box{
  display: flex;
  justify-content: center;
  align-items: center;
}
@media (max-width: 991px) {
  .project_box {
    display: block;
  }
  .img_pro {
   margin-top: 20px;
  }
}
</style>