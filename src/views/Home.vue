<template>
  <div class="main">
    <Header />
    <Intro />
    <div class="about">
      <v-container>
        <h1>More about me</h1>
        <p class="about-txt">
          I am a believer in smart work, and i love challenging my self a lot. I
          love engineering, science and technology. I am a holder of a bachelors
          of Engineering from the faculty of Engineering and technology in the
          university of Buea. Over the years in the university, i studied
          telecommunication engineering. During my studies i fell in love with
          computer programming and i learned C++, python and Javascript. I am a
          2years plus experienced Fullstack software developer in VueJs,
          ReactJs, NodeJs and Django. I also build mobile apps with
          Ionicframework. I am passionate about blockchain technology and as
          such, i also program in solidity, building smart contracts with the
          etherium technology. Over the years, i have been opportuned to gain
          profesional experience in the leadership, Business and software
          engineering. I was able to Voluteer at Yest-In as a frontend Vuejs
          Developer where we built a blood management system for my nation. I
          have also served as a software intern at Summit Tech for 4 Months. I
          am the lead software contractor at Etchi works where i manage software
          projects. I have worked for bridge africa ventures as a software
          engineer for a period of 1 Year. I am also the education Director of
          Nervtek in the silicon mountain, where i give back to my community by
          teaching computer programming and robotics (Internet Of Things).
          <br />
        </p>
        <span>
          My strengths are ; <br />
          💪 I love upgrading my skills in the said technologies above. <br />
          💪 I love learning new technologies. <br />
          💪 I accept critics in order to upgrade and better my self. <br />
          💪 I love challenges.
        </span>
      </v-container>
      <v-container>
        <v-card class="expertise animate__animated animate__fadeInDown">
          <div class="box">
            <v-icon class="icon" large color="#21b0f4"
              >mdi-rocket-launch</v-icon
            >
            <h3>Front-End Development</h3>
            <p>I love creating beatiful and interact user interfaces. 😎</p>
            <p class="heading">Web Tools</p>
            <p>React Js</p>
            <p>Vue Js</p>

            <p class="heading">Mobile Apps Tools</p>
            <p>React Native</p>
            <p>Ionic Vue</p>
            <p>Ionic React</p>
          </div>
          <div class="box mid">
            <v-icon class="icon" large color="#21b0f4">mdi-meditation</v-icon>
            <h3>Back-End Development</h3>
            <p>I am a backend genius as well 😊</p>
            <p class="heading">Dev Tools</p>
            <p>Django</p>
            <p>Express JS/Node</p>
            <p>PostgresSQL</p>
            <p>MySQL</p>
            <p>MongoDB</p>
            <p>AWS</p>
            <p class="heading">Devops</p>
            <p>Docker</p>
            <p>Kubernetes</p>
          </div>
          <div class="box">
            <v-icon class="icon" large color="#21b0f4"
              >mdi-hammer-screwdriver</v-icon
            >
            <h3>Blockchain Development</h3>
            <p>I so love the blockchain technology. 💥</p>
            <p class="heading">Dev Tools</p>
            <p>Solidity</p>
            <p>Moralis</p>
            <p>Truffle</p>
            <p>Ganache</p>
          </div>
        </v-card>

        <div class="projects">
          <h1>My Recent Work</h1>
          <p>Here are a few design projects I've worked on recently.</p>
          <v-row>
            <v-col v-for="(project, index) in projects" :key="index">
              <Project :project="project" />
            </v-col>
          </v-row>
        </div>
        <v-card color="#141C3A" class="resume-desk">
          <v-row>
            <v-col cols="3">
              <h1>Know more ?</h1>
            </v-col>
            <v-col>
              <p class="white--text">
                Know more about my education and work experience.
              </p>
            </v-col>
            <v-col cols="2">
              <v-btn
                to="/CV.pdf"
                target="_blank"
                color="white"
                depressed
                outlined
                rounded
              >
                See My Resume
              </v-btn>
            </v-col>
          </v-row>
        </v-card>
        <v-card color="#141C3A" class="resume-mobile">
          <v-col>
            <v-col>
              <p class="white--text">
                Know more about my education and work experience.
              </p>
            </v-col>
            <v-col class="btn-m">
              <v-btn
                to="/CV.pdf"
                target="_blank"
                color="white"
                depressed
                outlined
                rounded
              >
                See My Resume
              </v-btn>
            </v-col>
          </v-col>
        </v-card>

        <div class="colab">
          <h5>I'm proud to have collaborated with some awesome companies:</h5>
          <div class="companies">
            <span
              class="company"
              v-for="(company, index) in companies"
              :key="index"
            >
              <img :src="company" alt="" class="img-cmp" />
            </span>
          </div>
        </div>
      </v-container>

      <div class="footer">
        <v-container class="links">
          <h1>Start a project with me today!</h1>
          <p>Living, learning, & leveling up one day at a time.</p>
          <v-row>
            <v-btn
              href="https://github.com/Sir-Deon"
              target="_blank"
              depressed
              outlined
              fab
              color="white"
            >
              <v-icon>mdi-github</v-icon>
            </v-btn>
            <div style="width: 10px"></div>
            <v-btn
              href="https://www.linkedin.com/in/deon-achuo-251087188/"
              target="_blank"
              depressed
              outlined
              fab
              color="white"
            >
              <v-icon>mdi-linkedin</v-icon>
            </v-btn>
            <div style="width: 10px"></div>
            <v-btn
              href="https://twitter.com/TDenisdeon"
              target="_blank"
              depressed
              outlined
              fab
              color="white"
            >
              <v-icon>mdi-twitter</v-icon>
            </v-btn>

            <div style="width: 10px"></div>
            <v-btn
              href="https://www.youtube.com/channel/UCaLoHRK7dmAvYN1G02NFa9Q "
              target="_blank"
              depressed
              outlined
              fab
              color="white"
            >
              <v-icon>mdi-youtube</v-icon>
            </v-btn>
          </v-row>
        </v-container>
      </div>
    </div>
  </div>
</template>

<script>
import "animate.css";
import Header from "../components/Header.vue";
import Project from "../components/Project.vue";
import Intro from "../components/Intro.vue";
export default {
  name: "Home",
  data: () => ({
    companies: [
      "/nervtek.png",
      "/ngt.jpeg",
      "/yestin.png",
      "/bav.png",
      "/etchiworks.png",
      "/summit.jpeg",
      "/nufisoft.jpeg",
    ],

    projects: [
      {
        title: "Learners Grasp",
        description: ` An E-Learning Platform to help students prepare for exams. This is an
            app that brings teachers to students.  This is a freelence fullstack project i single handedly built with ReactJs and NodeJs for a client.
            This project allows students to buy lessons and take them at their pace.`,
        technologies: [
          "👉 NodeJs",
          "👉 VueJS",
          "👉 NuxtJS",
          "👉 Socket.Io",
          "👉 AWS(S3)",
          "👉 Digital Ocean",
          "👉 MongoDB",
          "👉 Mailgun",
        ],
        pics: [
          "/leanersGrasp.png",
          "/login.png",
          "/student.png",
          "/teacher.png",
          "/library.png",
        ],
        repo: "",
        launch: "https://learnersgrasp.com/",
      },
      {
        title: "Blood Management System",
        description: ` A blood management system that is geared at saving lives. This app helps blood seekers get blood donors.
			this is the project i realised with a team of skilled developers like my self. 	During my volunteering period at Yest-In, i was opportuned to be the main frontend developer on this
			product.
			This project is a Vuejs powered application to help improve quality of health in my community.
			It helps blood donors to safely donate blood at hospitals operating under this system.`,
        technologies: [
          "👉 Flask",
          "👉 VueJS",
          "👉 NuxtJS",
          "👉 Socket.Io",
          "👉 Heroku",
          "👉 Digital Ocean",
          "👉 MongoDB",
          "👉 MySQL Database",
        ],
        pics: [
          "/main-page.png",
          "/dhs-dash-board.png",
          "/dhs.png",
          "/dhsmain.png",
          "/viewandupdate.png",
        ],
        repo: "",
        launch: "https://dh-service.org/",
      },
      {
        title: "Nervtek Online Payment Platform",
        description: `A simple React and NodeJS powered plartform for processing payments for
            registration of events for nervtek.`,
        technologies: [
          "👉 Firebase",
          "👉 MongoDB",
          "👉 VueJs",
          "👉 Heroku",
          "👉 NodeJS",
        ],
        pics: ["/main.png", "/nervtekpay.png", "/create.png", "/mtn.png"],
        repo: "",
        launch: "https://nervtek-registration.web.app/",
      },
      {
        title: "Open Talk",
        description: `This is a demo react native project.`,
        technologies: ["👉 React Native CLI"],
        pics: [
          "/opentalk1.png",
          "/opentalk2.png",
          "/opentalk3.png",
          "/opentalk4.png",
          "/opentalk5.png",
          "/opentalk6.png",
          "/opentalk7.png",
          "/opentalk8.png",
        ],
        repo: "https://github.com/Sir-Deon/OpenTalk",
        launch: "",
      },
      {
        title: "Tesla Clone",
        description: `This is a demo react native project.`,
        technologies: ["👉 React Native expo"],
        pics: ["/tesla.jpeg"],
        repo: "https://github.com/Sir-Deon/Tesla-clone",
        launch: "",
      },
      {
        title: "Crytoverse",
        description: `Out of my urge to learn about crypto i got to understand Rapid API with the help of youtube, by building this  Demo crypto info application`,
        technologies: ["👉 ReactJs", "👉 Rapid Api", "👉 Redux Toolkit"],
        pics: [
          "/crypto.png",
          "/cryptoverse.png",
          "/crypto2.png",
          "/crypto3.png",
        ],
        repo: "https://github.com/Sir-Deon/cryptoverse",
        launch: "https://mycryptoapp-1b9f0.web.app",
      },
    ],
  }),
  components: {
    Header,
    Project,
    Intro,
  },
  methods: {
    openLink() {
      alert("weioufg");
    },
  },
};
</script>

<style scoped>
.intro {
  display: grid;
  place-items: center;
}

.greetings {
  font-family: "Russo One";
  font-weight: Bold;
  font-size: 50px;
}
.position {
  margin-top: 20px;
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
}

img {
  border-radius: 100px;
  width: 30%;
}

.about {
  background-color: #21b0f4;
  color: white;
  height: 500px;
}

.about-txt {
  text-align: justify;
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
  color: #fff;
}
span {
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
}

.expertise {
  display: flex;
  padding: 10px;
}

.box {
  width: 100%;
  display: grid;
  place-items: center;
  min-height: 200px;
}
.box h3 {
  margin-top: 10px;
}

.box p {
  text-align: center;
  width: 60%;
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
}
.mid {
  border-left: solid 1px #ccc;
  border-right: solid 1px #ccc;
}
.icon {
  height: 60px;
}
.heading {
  color: #21b0f4;
}

.projects h1,
p {
  text-align: center;
  color: black;

  margin-top: 20px;
}
.projects p {
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
}
.resume-desk {
  padding: 20px;
  color: #fff;
  display: block;
}
.resume-mobile {
  display: none;
}
h1,
h5 {
  font-family: "Russo One";
}

.resume-desk p {
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
}
.colab {
  display: grid;
  place-items: center;
}

.colab h5 {
  color: black;
  font-size: 20px;
  margin-top: 20px;
}
.companies {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  margin-left: 260px;
  padding: 20px;
}
.company {
  width: 30%;
}
.company img {
  width: 30%;
  height: 30%;
}

.footer {
  width: 100%;
  min-height: 200px;
  background-color: #21b0f4;
}

.footer p {
  color: #fff;
}

.links {
  display: grid;
  place-items: center;
}

@media screen and (max-width: 480px) {
  .about {
    min-height: 1000px;
  }
  .expertise {
    flex-wrap: wrap;
  }
  .mid {
    border-left: none;
    border-right: none;
    border-top: solid 1px #ccc;
    border-bottom: solid 1px #ccc;
  }
  .resume-desk {
    display: none;
  }
  .resume-mobile {
    display: block;
  }
  .btn-m {
    display: flex;
    align-items: center;
  }
  .btn-m .v-btn {
    margin-left: 60px;
  }
  .footer {
    width: 100%;
    min-height: 250px;
    background-color: #21b0f4;
  }
  .companies {
    margin-left: 100px;
    display: flex;
  }
  .colab h5 {
    color: black;
    font-size: 20px;
    text-align: center;
  }
  .company {
    width: 50%;
  }
}
</style>
