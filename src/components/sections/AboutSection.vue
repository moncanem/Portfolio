<template>
  <section id="about">
    <figure class="row">
      <img :src="photoOfMe" />
      <figcaption>
        <h1>About Me</h1>
        <p>
          Motivated and detail-oriented web development student with a strong
          desire to learn and develop new skills. Experienced in administrative
          support and recruitment. Fluent in four languages - Slovak, Czech,
          English, and Italian. Known for strong analytical and problem-solving
          skills, attention to detail, and excellent time management. Passionate
          about web development and eager to contribute expertise to dynamic
          projects.
        </p>

        <!-- LINKS -->
        <section class="titles">
          <p
            class="links"
            :class="{ active: activeTab === 'skills' }"
            @click="setActiveTab('skills')"
          >
            Skills
          </p>
          <p
            class="links"
            :class="{ active: activeTab === 'experience' }"
            @click="setActiveTab('experience')"
          >
            Experience
          </p>
          <p
            class="links"
            :class="{ active: activeTab === 'education' }"
            @click="setActiveTab('education')"
          >
            Education
          </p>
        </section>
        <!-- LINKS END -->

        <!-- CONTENT -->
        <section class="content active-content" v-if="activeTab === 'skills'">
          <figure>
            <img :src="office" />
            <img :src="html" />
            <img :src="css" />
            <img :src="bootstrap" />
            <img :src="js" />
          </figure>
          <figure>
            <img :src="react" />
            <img :src="vue" />
            <img :src="php" />
            <img :src="wordpress" />
            <img :src="github" />
          </figure>
        </section>
        <section class="content" v-else-if="activeTab === 'experience'">
          <article>
            <h4>School Projects</h4>
            <span>Tamwood College, January 2023 - July 2023</span>
          </article>
          <ul>
            <li>
              Actively participated in various school projects focused on web
              development
            </li>
            <li>
              Actively participated in various school projects focused on web
              development
            </li>
            <li>
              Built visually appealing and responsive websites using HTML,
              CSS/SCSS, JavaScript, and PHP
            </li>
            <li>
              Demonstrated proficiency in utilizing JavaScript frameworks and
              PHP programming language
            </li>
            <li>
              Assumed the role of team leader for select projects, overseeing
              code reviews and managing GitHub repositories
            </li>
            <li>
              Strengthened technical skills, teamwork, and project management
              abilities through hands-on experience
            </li>
          </ul>
        </section>
        <section class="content" v-else-if="activeTab === 'education'">
          <article>
            <h4>Diploma: Web Development</h4>
            <span class="edu"
              >Tamwood Careers College - Vancouver, BC<br />January 2023 -
              Current</span
            >
          </article>
          <article>
            <h4>Bachelor in Translation Interpreting studies</h4>
            <span class="edu"
              >Comenius University - Bratislava, Slovakia<br />September 2019 -
              May 2022</span
            >
          </article>
        </section>
        <!-- CONTENT END -->
      </figcaption>
    </figure>
  </section>
</template>

<script>
import photoOfMe from "../../img/me.jpg";
import office from "../../img/office (1).png";
import html from "../../img/html-5.png";
import css from "../../img/css-3 (1).png";
import bootstrap from "../../img/bootstrap (1).png";
import js from "../../img/js.png";
import react from "../../img/physics.png";
import vue from "../../img/brands.png";
import php from "../../img/php.png";
import wordpress from "../../img/wordpress.png";
import github from "../../img/github (2).png";
export default {
  name: "AboutSection",
  data() {
    return {
      activeTab: "skills",
      photoOfMe: photoOfMe,
      office: office,
      html: html,
      css: css,
      bootstrap: bootstrap,
      js: js,
      react: react,
      vue: vue,
      php: php,
      wordpress: wordpress,
      github: github,
    };
  },
  methods: {
    setActiveTab(tab) {
      this.activeTab = tab;
    },
  },
};
</script>

<style>
#about {
  padding: 5% 80px 0 10%;
  color: #355070;
}

.row img {
  width: 35%;
  border-radius: 15px;
}

.row {
  display: flex;
  column-gap: 5vh;
  /* flex-wrap: wrap; */
}

.row figcaption {
  display: flex;
  flex-direction: column;
  row-gap: 1vh;
}

.row h1 {
  font-size: 35px;
  font-weight: 600;
  display: flex;
}

.row p {
  text-align: justify;
  font-size: 18px;
  line-height: 1.5;
}

.titles {
  display: flex;
  padding: 20px 0 30px;
}

.links {
  padding-right: 50px;
  font-size: 18px;
  font-weight: 500;
  cursor: pointer;
  position: relative;
}

.links::after {
  content: "";
  width: 0;
  height: 3px;
  background: #dd6e6e;
  position: absolute;
  left: 0;
  bottom: -8px;
  transition: 0.4s;
}

.links.active::after {
  width: 30%;
}

.content figure {
  display: flex;
  column-gap: 2vh;
  width: 40%;
}

.content h4 {
  color: #dd6e6e;
  font-size: 20px;
  display: flex;
}

.content span {
  display: flex;
  font-size: 18px;
}

.content article {
  padding-bottom: 10px;
}

.content ul {
  padding: 0 0 3% 40px;
  text-align: justify;
  font-size: 16px;
}

.content.active-content {
  display: flex;
  flex-direction: column;
  row-gap: 5vh;
  justify-content: center;
}
   
   
/***** DARK MODE *****/
.dark-mode #about {
    color:#4e75a5;
}

.dark-mode .content ul {
    /* color: #F6F4F1; */
    color: rgb(179, 179, 179);
}

.dark-mode .content span {
    color: #dd6e6e;
    /* color: #d98e8e; */
}

.dark-mode .content .edu {
    color: rgb(179, 179, 179);
}
</style>