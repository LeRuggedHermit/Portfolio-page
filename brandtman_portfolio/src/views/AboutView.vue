<template>
  <main>
<article class="academics">
  <h1>Academic background:</h1>

  <h3>The Mid Sweden University <i>- 2022-2024</i></h3>
  <h4>
    <i>Higher Education Diploma with specialization in Computer Engineering </i>
  </h4>

  <h3>Örebro University <i>- 2020-2022</i></h3>
  <h4>
    <i>Legal Science with an International and Digital specialization. partially finished.</i>
  </h4>

  <h3>Linnaeus University <i>- summer 2022</i></h3>
  <h4>
    <i>
      Science Fiction and Extraterrestrial Life, Literature Studies - Independent Course
    </i>
  </h4>

  <h3>
    University of Stockholm <i>- summer 2024</i>
  </h3>

  <h4>
    <i>
      Dinosaurs - Their Evolution and Extinction, Introductory Course, Geology - Independent Course
    </i>
    <br>
    <br>
    <i>
      Egyptologi, archeology - Independent course.
    </i>
  </h4>
</article>


<article class="technologies">

  <h1>My technologies:</h1>

  <div class="tech-wrap">
  <div class="tech">
  <h3>Programming Languages</h3>
<h4>HTML</h4>
<h4>CSS</h4>
<h4>JavaScript</h4>
<h4>PHP</h4>
<h4>C#</h4>
<h4>.Net</h4>
<h4>SQL</h4>
<h4>Python</h4>
<h4>TypeScript</h4>
</div>

<div class="tech">
<h3>Frontend Frameworks</h3>
<h4>Vue.JS</h4>
<h4>Angular</h4>
<h4>React</h4>
</div>


<div class="tech">
<h3>Backend Frameworks</h3>
<h4>Laravel</h4>
<h4>Express</h4>
</div>

<div class="tech">
<h3>Frontend Animation and Graphics Libraries</h3>
<h4>GSAP</h4>
<h4>Three.js</h4>
</div>

<div class="tech">
<h3>.NET Family</h3>
<h4>.NET (6, 7, 8)</h4>
<h4>ASP.NET Core</h4>
<h4>ASP.NET MVC</h4>
<h4>Entity Framework</h4>
</div>

<div class="tech">
<h3>CSS Frameworks/Preprocessors</h3>
<h4>SASS</h4>
<h4>Stylus</h4>
<h4>SCSS</h4>
<h4>Materialize</h4>
<h4>Bootstrap</h4>
<h4>Tailwind</h4>
</div>

<div class="tech">
<h3>Development Tools</h3>
<h4>Node.js</h4>
<h4>Git</h4>
<h4>Postman</h4>
<h4>Thunderclient</h4>
</div>

<div class="tech">
<h3>Programming Environments</h3>
<h4>Visual Studio Code</h4>
<h4>Microsoft Visual Studio</h4>
<h4>Pycharm</h4>
</div>


<div class="tech">
<h3>Database Management Systems</h3>
<h4>MySQL</h4>
<h4>MongoDB</h4>
<h4>MariaDB</h4>
</div>

<div class="tech">
<h3>Design and Media Tools</h3>
<h4>Figma</h4>
<h4>Photoshop</h4>
<h4>Photopea</h4>
<h4>OBS Studio</h4>
<h4>Draw.io</h4>
</div>

<div class="tech">
<h3>Web Server</h3>
<h4>Xampp</h4>
</div>

<div class="tech">
<h3>Game Development Environment</h3>
<h4>Unity</h4>
</div>

<div class="tech">
<h3>Content Management System (CMS)</h3>
<h4>WordPress</h4>
</div>
</div>
</article>
  </main>
</template>

<style>
main{
  margin-top: 4rem;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-content: center;
  align-items: center;
}

article{
  width: 80%;
}

.technologies{
  margin-top: 5rem;
  margin-bottom: 2rem;
}

.technologies h1{
  text-align: center;
}

.tech-wrap{
  display: flex;
  flex-direction: row;
  justify-content: center;
  flex-wrap: wrap;
  gap: 4vmin;
  color: white;
}

.tech{
  width: 25%;
  background-color: rgb(70, 74, 116);
  padding: 4vmin;
}

.tech h3{
  font-size: 22px;
  text-align: center;
  text-decoration: underline;
}

@media screen and (max-width: 600px){

  .tech{
  width: 45%;
  background-color: rgb(70, 74, 116);
  padding: 4vmin;
}

  .tech h3{
  font-size: 16px;
  }

  .tech h4{
    font-size: 12px;
  }

  .technologies{
  margin-bottom: 8rem;
}
}

@media screen and (min-width: 601px) and (max-width: 840px){
  .tech{
  width: 45%;
  background-color: rgb(70, 74, 116);
  padding: 4vmin;
}

  .tech h3{
  font-size: 18px;
  }

  .tech h4{
    font-size: 14px;
    text-align: center;
  }

  .technologies{
  margin-bottom: 8rem;}
}
</style>
