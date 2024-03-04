<template>
  <div class="about">
    <div class="container">
      <div class="col-md-12 mt-5">
        <h1 class="text_about">About</h1>
      </div>
      <hr>
      <div class="description d-flex justify-content-center pt-2">
      <div class="col-md-6 text_about mb-2">
        <h3 class="text_about">Who I Am:</h3>
        Hello, I'm Pham Quang Phuc, but you can simply call me Mac. 
        I am a programmer who is always eager to accumulate practical experience and possesses a passion for constantly pushing the boundaries in the field of information technology.
      </div>
      <div class="col-md-6 text_about mb-2">
        <h3 class="text_about">Prizes</h3>
        <ul>
          <li>Prospective prize in Data-centric AI Competition 2021 (FPT Software).</li>
          <li>Consolation prize in University-level undergraduate research 2022 – 2023.</li>
          <li>Scholarship for the academic year 2022 – 2023</li>
        </ul>
      </div>
      </div>
    </div>
    <div class="container my-5">
      <h2 align="center" class="text_about">My Skills</h2>
      <hr>
      <div v-for="skill in skills" class="col-md-12 my-3 jr_skills text-center p-3">
        <h3 class="my-2">{{ skill.title }}</h3>
        <div class="my-2 d-flex justify-content-center align-items-center pt-3">
          <div v-for="item in skill.items" :key="item.name" class="skill_container">
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
          title: "Markup Languages & Style Sheet Languages",
          items: [
            {
              name: "HTML",
              icon: require("@/assets/icon/html5-original.svg"),
            },
            {
              name: "CSS",
              icon: require("@/assets/icon/css3-original.svg"),
            },
          ],
        },
        {
          title: "Programming Languages",
          items: [
            {
              name: "JavaScript",
              icon: require("@/assets/icon/javascript-original.svg"),
            },
            {
              name: "PHP",
              icon: require("@/assets/icon/php-original.svg"),
            },
            {
              name: "Python",
              icon: require("@/assets/icon/python-original.svg"),
            },
          ],
        },
        {
          title: "Frameworks",
          items: [
            {
              name: "Vue.js",
              icon: require("@/assets/icon/vuejs-original.svg"),
            },
            {
              name: "Laravel",
              icon: require("@/assets/icon/laravel-original.svg"),
            },
            {
              name: "Bootstrap",
              icon: require("@/assets/icon/bootstrap-original.svg"),
            }
          ],
        },
        {
          title: "Database",
          items: [
            {
              name: "MySQL",
              icon: require("@/assets/icon/mysql-original.svg"),
            },
            {
              name: "MS SQL",
              icon: require("@/assets/icon/microsoftsqlserver-original.svg"),
            },
          ],
        },
        {
          title: "Version Control",
          items: [
            {
              name: "Git",
              icon: require("@/assets/icon/git-original.svg"),
            },
            {
              name: "GitHub",
              icon: require("@/assets/icon/github-original.svg"),
            }
          ],
        }, 
        {
          title: "Tools",
          items: [
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
            {
              name: "Jupyter",
              icon: require("@/assets/icon/jupyter-original.svg"),
            },
          ],
        },
      ],
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
}
.jr_skills .skill_name {
  font-size: 1rem;
  color: #605858;
  font-weight: bold;
}
@keyframes heartbeat {
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
}
</style>
