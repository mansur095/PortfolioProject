<script setup scoped>
import folder from '../../public/folder1.svg'
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
  <section class="ide-section" id="details">
    <!-- Левая панель -->
    <aside class="sidebar">
      <div class="dir-title">details</div>
      <ul class="dir-list">
        <li class="dir-folder open">>
          <img
            :src="folder"
            alt="html"
            class="logo-folder"
          />
            <span class="info-bio">projects</span>
          </li>
          </ul>
    </aside>

    <!-- Центральная панель -->
    <div class="editor">
      <div class="editor-header">
        <span class="dot red"></span>
        <span class="dot yellow"></span>
        <span class="dot green"></span>
        <span class="editor-title">about-me</span>
      </div>
      <pre class="editor-content">
/**
<span class="green-text"> * About Project</span>
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
 * целостности видения. Однако сам процесс разработки принёс мне много удовольствия - особенно
 * когда удавалось находить элегантные решения сложных задач и наблюдать, как проект постепенно 
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
 */
      </pre>
      </div>

    <!-- Правая панель -->
    <div class="post-card details-card">
        <div v-for="(photo, index) in photos" :key="index" class="photo">
            <img 
                :src="photo.url" 
                :alt="photo.alt" 
                class="project"
            >
            <a 
                :href="photo.link" 
                class="project-button"
                target="_blank"
                rel="noopener noreferrer"
            >{{ photo.buttonText }}</a>
        </div>
    </div>
  </section>
</template>

<style scoped>
.ide-section {
    display: flex;
    flex-direction: row;
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
    position: relative;
}
.dir-folder.open {
    color: #fff;
    background: #22304a;
    border-radius: 4px;
    padding-left: 6px;
}
.logo-folder {
    width: 1.2vw;
    position: absolute;
    left: 6%;
    bottom: -15%;
}
.info-bio {
      margin-left: 15px;
}
.info-int {
    margin-left: 20px;
}
.info-ed {
    margin-left: 40px;
}
.arrow-down {
    position: absolute;
    left: 0%;
    bottom: 68%;
}
.dir-file {
    position: relative;
    margin-top: 8px;
    margin-left: 18px;
    color: #bfc9d1;
    font-size: 14px;
}
.open-folder {
    list-style: none;
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
.green { background: #27c93f42; }
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
.green-text { 
    color:#217769;
    font-size: 1rem;
}
.details-content h3, .details-content h4 {
    color: #8be9fd;
    margin: 10px 0 4px 0;
}
.details-content ul {
    margin: 0 0 10px 18px;
    padding: 0;
}
.details-content a {
    color: #50fa7b;
    text-decoration: underline;
}
.post-card.details-card {
    min-width: 25vw;
    max-width: 35vw;
    background: #182235;
    padding: 18px 22px;
    color: #bfc9d1;
    border: 2px solid #081c2c;
    display: grid;
    gap: 0px; /* Расстояние между фото */
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
}
.photo:nth-child(even) {
  margin-left: 10px;
}
.photo:nth-child(odd) {
  margin-right: 10px;
}
.project {
    width: 15vw;
    height: 15vh;
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