<script setup scoped>
// language img
import js from '../../public/js.svg'
import vue from '../../public/vue.svg'
import ts from '../../public/typescript.svg'
import css from '../../public/css.svg'
import html from '../../public/html.svg'
import git from '../../public/git.svg'
import github from '../../public/github.svg'

// folder img
import folder from '../../public/folder1.svg'
import folder2 from '../../public/folder2.svg'
import folder3 from '../../public/folder3.svg'
import info from '../../public/info.svg'

import projectOne from '../assets/project-one.png'
import projectTwo from '../assets/project-two.png'
import projectThree from '../assets/project-three.png'
import projectFour from '../assets/project-four.png'
import projectFive from '../assets/project-five.png'
import projectSix from '../assets/project-six.png'

const photos = [
{ url: projectOne, alt: "Описание 1", link: "https://github.com/mansur095/MyProjectPortfolio.ShoesShop", buttonText: "Подробнее" },
  { url: projectTwo, alt: "Описание 2", link: "https://github.com/mansur095/mansur095.github.io", buttonText: "Подробнее"  },
  { url: projectThree, alt: "Описание 3", link: "https://github.com/mansur095/tictactoe.game", buttonText: "Подробнее"  },
  { url: projectFour, alt: "Описание 4", link: "https://github.com/mansur095/Project.Shoes", buttonText: "Подробнее"  },
  { url: projectFive, alt: "Описание 5", link: "https://github.com/mansur095/weather-web", buttonText: "Подробнее"  },
  { url: projectSix, alt: "Описание 6", link: "https://github.com/mansur095/MyProjectPortfolio.CompBuild", buttonText: "Подробнее"  },
];

</script>

<template>
  <section class="ide-section" id="info">
    <!-- Левая панель -->
    <aside class="sidebar">
      <div class="dir-title">personal-info</div>
      <ul class="dir-list">
        <li class="dir-folder open">>
            <span class="info-bio">bio 
              <img
                :src="folder"
                alt="html"
                class="logo-folder"
              /></span>
          </li>
        <li class="dir-folder">>
          <span class="info-int">education
            <img
            :src="folder2"
            alt="html"
            class="logo-folder two"
          />
          </span>
        </li>
        <li class="dir-folder">
          <span class="info-ed"><span class="arrow-down">˅</span>interests
            <img
            :src="folder3"
            alt="html"
            class="logo-open-folder"
          />
          </span>
          <ul class="open-folder">
            <li class="dir-file">
              <span class="info-folder">working
                <img
                  :src="info"
                  alt="html"
                  class="logo-info"
                />
              </span>
            </li>
            <li class="dir-file">
              <span class="info-folder">hobby
                <img
                  :src="info"
                  alt="html"
                  class="logo-info-two"
                />
              </span>
            </li>
          </ul>
        </li>
      </ul>
      <div 
        class="dir-title" 
        style="margin-top:2rem;" 
        id="contacts"
      >contacts</div>
      <div class="contacts-block">
        <div class="contact-item email">
          <span class="icon">@</span>
          <span>dev.mansurhus@mail.ru</span>
        </div>
      </div>
    </aside>

    <!-- Центральная панель -->
    <div class="editor">
      <div class="editor-header">
        <span class="dot red"></span>
        <span class="dot yellow"></span>
        <span class="dot green"></span>
        <span class="editor-title">bio</span>
      </div>
      <pre class="editor-content">
/**
 * About Me
<span class="green"> *   Welcome to my portfolio.</span>
 *
 * <span class="orange">[Front-end]</span> More than a hobby — it’s what drives me. I thrive on mastering new tools, 
 * building projects, and debugging challenges.
 * <span class="orange">[Self-Taught Developer]</span> ...
 * <span class="orange">[Programming]</span> My stack: HTML, CSS, JS, VUE, REACT, TS etc.
 *
 * <span class="blue">[Whoami]</span> Code enthusiast on a never-ending learning journey. I blend into teams like a 
 * React hook into a component – smoothly and 
 *          effectively. My dev mantra: clean code first, magic second.
 *
<span class="green"> *   About Project</span>
 *
 * Мои проекты находятся в постоянной доработке и пока не достигли идеала, 
 * который я изначально задумывал. Однако они демонстрируют ключевые навыки 
 * современной frontend-разработки: работу с API (использовал для создания поиска фильмов),
 * построение SPA-приложений, а также интеграцию различных библиотек.
 *
 * Особенно мне понравилось работать с GSAP для создания плавных анимаций и Axios для удобной
 * работы с HTTP-запросами. В процессе разработки я уделял внимание:
 *   Улучшению читаемости кода (более понятная структура, осмысленные названия переменных)
 *   Оптимизации критических участков
 *   Добавлению комментариев в сложных местах, где могла возникнуть путаница
 *   Визуальным улучшениям интерфейса 
 *
 * Наибольшую сложность представляло проектирование архитектуры приложения и поддержание
 * целостности видения. Однако сам процесс разработки принёс мне много 
 * удовольствия - особенно
 * когда удавалось находить элегантные решения сложных задач и наблюдать, 
 * как проект постепенно 
 * становится лучше.
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 *
 */
      </pre>
    </div>

    <!-- Правая панель -->
    <div class="post-card">
      <div class="post-header">
        <div>
          <div class="username">@mansurhus</div>
          <div class="created">Created 5 month ago</div>
        </div>
        <div class="post-actions">
          <span>★ 18 stars</span>
        </div>
      </div>
      <div>
        <p>// Programming language and other programms </p>
      </div>
      <div class="post-body">
        <div class="skills-grid">
          <div class="skill checked">
            <img
              :src="html"
              alt="html"
              class="logo-language"
            />
            html
          </div>
          <div class="skill checked">
            <img
              :src="css"
              alt="html"
              class="logo-language"
            />
            css
          </div>
          <div class="skill checked">
            <img
              :src="js"
              alt="html"
              class="logo-language"
            />
            Javascript
          </div>
          <div class="skill checked">
            <img
              :src="ts"
              alt="html"
              class="logo-language"
            />
            typescript
          </div>
          <div class="skill checked">
            <img
              :src="vue"
              alt="html"
              class="logo-language"
            />
            vue
          </div>
          <div class="skill checked">
            <img
              :src="git"
              alt="html"
              class="logo-language"
            />
            git
          </div>
        </div>
      </div>
      <div class="post-card details-card">
        <div v-for="(photo, index) in photos" :key="index" class="photo">
            <img 
                :src="photo.url" 
                :alt="photo.alt" 
                class="project"
            >
            <a :href="photo.link" class="project-button">{{ photo.buttonText }}</a>
        </div>
    </div>
    </div>
  </section>
  <div class="footer-info">
    <div class="link left">
      <a href="https://github.com/mansur095" class="link-github">mansur-husainov</a>
    </div>
    <div class="link right">
      <a href="https://github.com/mansur095" class="link-github">@mansur095<img :src="github" alt="" class="icon"></a>
    </div>
  </div>
</template>

<style scoped>
.ide-section {
  display: flex;
  flex-direction: row;
  margin-top: 40px;
  min-height: 55vh;
  border: 2px solid #081c2c;
}
.sidebar {
  width: 15vw;
  background: #182235;
  padding: 18px 12px;
  color: #bfc9d1;
  font-size: 15px;
  display: flex;
  flex-direction: column;
  min-width: 5vw;
  border: 2px solid #081c2c;
}
.dir-title {
  font-weight: bold;
  color: #bfc9d1;
  margin-bottom: 8px;
  margin-top: 8px;
}
.dir-list {
  list-style: none;
  padding-left: 0;
  margin-bottom: 0;
}
.dir-folder {
  margin-bottom: 6px;
  letter-spacing: 2px;
  cursor: pointer;
  font-weight: 500;
  color: #f1fa8c;
}
.dir-folder.open {
  color: #fff;
  background: #22304a;
  border-radius: 4px;
  padding-left: 6px;
}
.dir-folder.air {
    margin-left:12px;
}
.info-bio {
  margin-left: 15px;
  position: relative;
}
.info-int {
  margin-left: 20px;
  position: relative;
}
.info-ed {
  margin-left: 40px;
  position: relative;
}
.arrow-down {
  position: absolute;
  left: -43%;
  bottom: 0%;
}
.dir-file {
  position: relative;
  margin-top: 8px;
  margin-left: 18px;
  color: #bfc9d1;
  font-size: 14px;
}
.contacts-block {
  margin-top: 10px;
}
.contact-item {
  display: flex;
  align-items: center;
  margin-bottom: 6px;
  color: #50fa7b;
  font-size: 14px;
}
.contact-item .icon {
  margin-right: 7px;
}
.editor {
  flex: 1;
  background: #1a2330;
  margin: 0;
  min-width: 20vw;
  max-width: 70vw;
  display: flex;
  flex-direction: column;
  border: 2px solid #081c2c;
}
.editor-header {
  display: flex;
  align-items: center;
  padding: 8px 16px;
  background: #182235;
  border-radius: 10px 10px 0 0;
  gap: 8px;
  border-bottom: 4px solid #081c2c;
}
.dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  display: inline-block;
  margin-right: 4px;
}
.red { background: #ff5f56; }
.yellow { background: #ffbd2e; }
.orange { color:#b36966;}
.blue { color: #37479f;}
.green-text { 
    color:#217769;
    font-size: 1rem;
}
.editor-title {
  margin-left: 16px;
  font-weight: bold;
  color: #bfc9d1;
}
.editor-content {
  background: none;
  color: #bfc9d1;
  font-family: 'Fira Mono', 'Consolas', monospace;
  font-size: 15px;
  padding: 18px 20px;
  border-radius: 0 0 10px 10px;
  min-height: 350px;
  white-space: pre-wrap;
}
.editor-content .green {
  color: #43958c;
  font-weight: bold;
}
.post-card {
  min-width: 35vw;
  max-width: 50vw;
  background: #182235;
  padding: 18px 22px;
  color: #bfc9d1;
  display: flex;
  flex-direction: column;
  gap: 12px;
  border: 2px solid #081c2c;
}
.post-header {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 10px;
}
.avatar {
  width: 44px;
  height: 44px;
  border-radius: 50%;
  object-fit: cover;
  background: #222;
}
.username {
  font-weight: bold;
  color: #3047a0;
}
.created {
  margin-top: 0.1rem;
  font-size: 12px;
  color: #6272a4;
}
.post-actions {
  margin-left: auto;
  display: flex;
  gap: 12px;
  font-size: 13px;
  color: #6272a4;
}
.post-body {
  margin-top: 8px;
}
.skills-grid {
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  gap: 8px 16px;
}
.skill {
  display: flex;
  align-items: center;
  gap: 7px;
  font-size: 1.2rem;
  color: #bfc9d1;
  background: #1a2330;
  border-radius: 6px;
  padding: 8px 4px;
}
.skill.checked {
  color: #fff;
  background: #22304a;
  font-weight: bold;
}
.logo-language{
  width: 2vw;
}
.logo-folder {
  width: 60%;
  position: absolute;
  left: -65%;
  bottom: -17%;
}
.logo-folder.two {
  width: 24%;
  left: -25%;
  bottom: -17%;
}
.logo-open-folder {
  width: 23%;
  position: absolute;
  left: -24%;
  top: -25%;
}
.info-folder {
  position: relative;
}
.logo-info {
  width: 25%;
  position: absolute;
  top: -20%;
  left: -30%;
}
.logo-info-two {
  width: 33.4%;
  position: absolute;
  bottom: 0%;
  left: -39%;
}
.open-folder {
  list-style: none;
}
.skill .icon {
  color: #50fa7b;
  font-size: 16px;
}
.footer-info {
  display: flex;
  justify-content: space-between;
  background: #182235;
}
.link {
  display: block;
  border: 4px solid #081c2c;
  border-top: 0;
  border-bottom: 0;
  padding: 8px 16px;
}
.link.left {
  width: 14.6vw;
}
.link.right {
  width: 37.9 vw
}
.link-github {
  text-decoration: none;
  color:#43958c;
  position: relative;
}
.icon {
  width: 20px;
  margin-left: 6px;
}
.post-card.details-card {
  min-width: 25vw;
  max-width: 35vw;
  background: #182235;
  padding: 18px 22px;
  color: #bfc9d1;
  display: grid;
  gap: 0px; /* Расстояние между фото */
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  border: 0;
}
.photo:nth-child(even) {
  margin-left: 10px;
}
.photo:nth-child(odd) {
  margin-right: 10px;
}
.project {
  border-radius: 8px; 
  width: 15vw;
  height: 16vh;
}
.project-button {
  display: inline-block;
  margin: 10px;
  padding: 8px 16px;
  background-color: #233649; /* Зеленый цвет */
  color: white;
  text-decoration: none;
  border-radius: 4px;
  transition: background-color 0.3s;
}
.project-button:hover {
  background-color: #1d2c3b; /* Темнее при наведении */
}
</style> 