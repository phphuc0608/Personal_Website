<template>
  <div class="about">
    <div class="container">
      <div class="col-md-12 mt-5">
        <h1 class="text_about">About</h1>
      </div>
      <hr>
      <div class="description pt-2">
        <div class="col-md-6 des_item text_about mb-2">
          <h3 class="text_about">Who I Am:</h3>
          I’m Mac, an Industry 4.0 Engineer at Universal Scientific Industrial Vietnam Co., Ltd., specializing in managing Continuous Improvement Projects (CIP) to enhance production efficiency and quality. 
          I also develop software for factory digitalization, leveraging tools like FlexSim, SketchUp, and programming skills to support digital transformation and operational excellence.
        </div>
        <div class="col-md-6 des_item text_about mb-2">
          <h3 class="text_about">Prizes</h3>
          <ul>
            <li>Prospective prize in Data-centric AI Competition 2021 (FPT Software).</li>
            <li>Consolation prize in University-level undergraduate research 2022 - 2023.</li>
            <li>Scholarship for the academic year 2022 - 2023</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="container my-5">
      <h2 align="center" class="text_about">My Skills</h2>
      <hr>
      <div v-for="skill in skills" class="col-md-12 my-3 jr_skills text-center p-3">
        <h3 class="my-2">{{ skill.title }}</h3>
        <div class="my-2 d-flex justify-content-center align-items-center pt-3 flex-wrap" style="gap: 15px">
          <div v-for="item in skill.items" :key="item.name" class="skill_container p-3">
            <img :src="item.icon" class="icon_skill" alt="">
            <div class="skill_name pt-2">{{ item.name }}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutView",
  data() {
    return {
      skills: [
        {
          title: "Project Management Skills",
          items:[
            {
              name:"Project Planning",
              icon:require("@/assets/icon/project_planning.gif")
            },
            {
              name:"Timeline Management",
              icon:require("@/assets/icon/timeline.gif")
            },
            {
              name:"Risk assessment",
              icon:require("@/assets/icon/risk.gif")
            },
            {
              name:"Team collaboration",
              icon:require("@/assets/icon/team_colab.gif")
            },
            {
              name:"Resources allocation",
              icon:require("@/assets/icon/resources.gif")
            },
            {
              name:"Client communication",
              icon:require("@/assets/icon/meeting.gif")
            },
          ]
        },
        {
          title: "Technical Skills",
          items: [
            {
              name: "Coding",
              icon: require("@/assets/icon/programmer.gif"),
            },
            {
              name: "Flexsim",
              icon: require("@/assets/icon/flexsim.png"),
            },
            {
              name: "Sketchup",
              icon: require("@/assets/icon/sketchup.svg"),
            },
          ],
        },
        {
          title: "Tools",
          items: [
            {
              name: "Microsoft Planner",
              icon: require("@/assets/icon/microsoft-planner.webp"),
            },
            {
              name: "Trello",
              icon: require("@/assets/icon/trello.png"),
            },
            {
              name: "VS Code",
              icon: require("@/assets/icon/vscode-original.svg"),
            },
            {
              name: "Figma",
              icon: require("@/assets/icon/figma-original.svg"),
            },
            {
              name: "Postman",
              icon: require("@/assets/icon/postman-original.svg"),
            },
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
#app{
  overflow: hidden;
}
.text_about {
  color: #F5F5F5;
  opacity: 1 !important;
}
.description {
  display: flex;
  justify-content: center;
}
hr {
  border: 1px solid #F5F5F5;
  margin: 1rem 0;
  opacity: .25;
}

.jr_skills {
  background-color: white;
  border-radius: 10px;
}

.jr_skills h3 {
  text-decoration: underline;
  font-weight: bold;
}
.jr_skills .skill_container {
  padding: 0 1rem;
}
.jr_skills .icon_skill {
  width: 45px;
  height: auto;
  color: #605858;
  animation: heartbeat 2s infinite;
  box-sizing: border-box;
}
.jr_skills .skill_name {
  font-size: 1rem;
  color: #605858;
  font-weight: bold;
}
/* @keyframes heartbeat {
  0% {
    transform: scale(1);
  }
  20% {
    transform: scale(1.1);
  }
  40% {
    transform: scale(1);
  }
  60% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(1);
  }
} */

@media (max-width: 720px) {
  .description {
    display: block;
  }
  .des_item {
    margin-top: 1rem;
  }
}
</style>
