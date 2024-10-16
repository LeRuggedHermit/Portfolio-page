<template>
     <!--andra sidbanner: -->
     <div class="second-banner">
            <ul class="skills">
              <li class="skill"><h3>Front-end</h3></li>
              <li class="skill"><h3>Back-end</h3></li>
              <li class="skill"><h3>HTML</h3></li>
              <li class="skill"><h3>CSS</h3></li>
              <li class="skill"><h3>Javascript</h3></li>
              <li class="skill"><h3>PHP</h3></li>
              <li class="skill"><h3>Typescript</h3></li>
              <li class="skill"><h3>Node.js</h3></li>
              <li class="skill"><h3>SASS</h3></li>
              <li class="skill"><h3>Less</h3></li>
              <li class="skill"><h3>Stylus</h3></li>
              <li class="skill"><h3>Bootstrap</h3></li>
              <li class="skill"><h3>Tailwind</h3></li>
              <li class="skill"><h3>GSAP</h3></li>
              <li class="skill"><h3>Wordpress</h3></li>
              <li class="skill"><h3>Laravel</h3></li>
              <li class="skill"><h3>Vue.js</h3></li>
              <li class="skill"><h3>React</h3></li>
              <li class="skill"><h3>Next.js</h3></li>
              <li class="skill"><h3>Vite</h3></li>
              <li class="skill"><h3>.NET</h3></li>
              <li class="skill"><h3>C#</h3></li>
              <li class="skill"><h3>Responsive webdesign</h3></li>
              <li class="skill"><h3>Accessability</h3></li>
              <li class="skill"><h3>Figma</h3></li>
              <li class="skill"><h3>API</h3></li>
              <li class="skill"><h3>Photoshop</h3></li>
              <li class="skill"><h3>Three.js</h3></li>
          </ul>  
          <ul class="skills" aria-hidden="true">
            <li class="skill"><h3>Front-end</h3></li>
            <li class="skill"><h3>Back-end</h3></li>
            <li class="skill"><h3>HTML</h3></li>
            <li class="skill"><h3>CSS</h3></li>
            <li class="skill"><h3>Javascript</h3></li>
            <li class="skill"><h3>PHP</h3></li>
            <li class="skill"><h3>Typescript</h3></li>
            <li class="skill"><h3>Node.js</h3></li>
            <li class="skill"><h3>SASS</h3></li>
            <li class="skill"><h3>Less</h3></li>
            <li class="skill"><h3>Stylus</h3></li>
            <li class="skill"><h3>Bootstrap</h3></li>
            <li class="skill"><h3>Tailwind</h3></li>
            <li class="skill"><h3>GSAP</h3></li>
            <li class="skill"><h3>Wordpress</h3></li>
            <li class="skill"><h3>Laravel</h3></li>
            <li class="skill"><h3>Vue.js</h3></li>
            <li class="skill"><h3>React</h3></li>
            <li class="skill"><h3>Next.js</h3></li>
            <li class="skill"><h3>Vite</h3></li>
            <li class="skill"><h3>.NET</h3></li>
            <li class="skill"><h3>C#</h3></li>
            <li class="skill"><h3>Responsive webdesign</h3></li>
            <li class="skill"><h3>Accessability</h3></li>
            <li class="skill"><h3>Figma</h3></li>
            <li class="skill"><h3>API</h3></li>
            <li class="skill"><h3>Photoshop</h3></li>
            <li class="skill"><h3>Three.js</h3></li>
        </ul> 
        </div>
</template>

<script>
export default{
    name: 'siteBanner_2',

}
</script>

<style scoped>
.second-banner {
  width: 100%;
  height: 220px;
  display: flex;
  flex-direction: row;
  align-items: center;
  align-content: center;
  gap: 12vmin;
  overflow: hidden;
  color: white;
  background-color: black;
  font-family: "Barlow Semi Condensed", sans-serif;
  font-weight: 200;
  font-size: 31.6px;
  margin-bottom: 5rem;
}

@keyframes scroll {
  to {
    transform: translateX(-100%);
  }
}

.skills {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  align-content: center;
  gap: 20vmin;
  list-style: none;
  animation: scroll 120s linear infinite;
}

.skill {
  width: fit-content;
}
</style>