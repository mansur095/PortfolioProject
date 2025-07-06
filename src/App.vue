<script setup lang="ts">
import GlitchText from './components/GlitchText.vue';
import Keyboard3D from './components/Keyboard3D.vue';
import InfoSection from './components/PersonalInfoSection.vue'
// Пока без логики, только разметка и стили
</script>

<template>
  <div class="background">
    <nav class="navbar">
      <div class="navbar-left">mansur-husainov</div>
      <div class="navbar-center">
        <a href="#hello" class="nav-link active">_hello</a>
        <a href="#info" class="nav-link">_about-me</a>
        <a href="#details" class="nav-link">_projects</a>
      </div>
      <div class="navbar-right">
        <a href="#contacts" class="nav-link">_contact-me</a>
      </div>
    </nav>
    <div class="main-flex">
      <main class="main-content">
        <div class="intro-text">
          <div class="greeting"><GlitchText
            :texts="['ПРИВЕТ', 'HELLO', 'HI', 'Bonjour', 'Hola']"
            :durationMs="1500"
            :holdMs="1000"
            :fps="40"
          /> all. I am</div>
          <div class="name">Mansur Husainov</div>
          <div class="role">&gt; Front-end developer</div>
        </div>

        <!-- info about me -->
        <pre class="contacts-code">
<span class="comment">// my Name</span>
<span class="change-text">const</span> <span class="var">name</span> = <span class="value">Mansur</span>;

<span class="comment">// my Surname</span>
<span class="change-text">const</span> <span class="var">surname</span> = <span class="value">Husainov</span>;

<span class="comment">// year of experience</span>
<span class="change-text">const</span> <span class="var">yearOfExperience</span> = <span class="value">2</span>;

<span class="comment">// my e-mail</span>
<span class="change-text">const</span> <span class="var">email</span> = <span class="string">"dev.mansurhus@mail.ru"</span>;

<span class="comment">// you can check my GitHub</span>
<span class="change-text">const</span> <span class="var">GitHub</span> = <span class="string">"https://github.com/mansur095"</span>;
        </pre>
      </main>
      <div class="three-container">
        <Keyboard3D class="keyboard" />
      </div>
    </div>
     <InfoSection></InfoSection>
  </div>
</template>

<style scoped>
.background {
  min-height: 100vh;
  width: 99vw;
  background: radial-gradient(ellipse at 60% 30%, #2e4857 0%, #1a2330 60%, #101624 100%);
  position: relative;
  font-family: 'Fira Mono', 'Consolas', monospace;
  color: #e6e6e6;
}
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #182235; /* тёмный фон */
  padding: 0.5rem 1rem;
  font-family: monospace;
  border: 2px solid #081c2c;
}

.navbar-left,
.navbar-center,
.navbar-right {
  display: flex;
  align-items: center;
}

.navbar-center {
  gap: 1rem;
}

.nav-link {
  color: #a9b1d6;
  text-decoration: none;
  padding: 0.5rem 1rem;
  border: 1px solid rgba(255, 255, 255, 0.1); /* лёгкая граница */
  border-radius: 4px;
  transition: all 0.3s ease;
  font-family: monospace;
  font-size: 14px;
}

.nav-link:hover {
  border-color: #ffffff55;
}

.nav-link.active {
  border-bottom: 2px solid #ffcc99; /* светлая подчеркивающая линия */
  color: #ffffff;
}
.main-flex {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: flex-start;
  gap: 256px;
  margin-bottom: 45vh;
}
.three-container {
  background-color: #0d1b2a;
  background-image: url('/public/tech-bg.jpg');
  /* 3️⃣ Смешиваем цвет и картинку */
  background-blend-mode: multiply; /* или overlay, darken, soft-light… */
  min-width: 40%;
  min-height: 485px;
  margin-top: 7vh;
  margin-right: 20vh;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 15px 15px 0px rgb(6, 12, 19);
  border: 2px solid #0d1b2a;
}

.main-content {
  margin: 80px 5vw 0 auto;
  max-width: 700px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
.intro-text {
  margin-bottom: 32px;
}
.greeting {
  font-size: 1.1rem;
  color: #bfc9d1;
  margin-bottom: 8px;
}
.name {
  font-size: 3rem;
  font-family: 'Fira Mono', 'Consolas', monospace;
  font-weight: bold;
  color: #fff;
  margin-bottom: 8px;
}
.role {
  font-size: 1.5rem;
  color: #4e6cf0;
  margin-bottom: 32px;
}
.contacts-code {
  background: none;
  color: #bfc9d1;
  font-size: 1.1rem;
  padding: 0;
  margin: 0;
}
.comment {
  color: #475c6e;
  margin-bottom: 100rem;
}
.change-text {
  color: #5498f1;
}
.var {
  color: #4ef0c7;
}
.value {
  color: #fff;
}
.string {
  color: #f7b267;
}
@media(max-width:1780px) {
  .three-container {
    margin-right: 0;
  }
}
</style>
