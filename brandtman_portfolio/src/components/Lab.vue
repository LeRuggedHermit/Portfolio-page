<template>
  <article class="content-container-2" id="lab">
  <section class="content">
    <!-- Projekt-Tab knappar -->
    <div class="project-tab">
      <button 
        class="p-tab" 
        :class="{ 'current': activeProject === index }" 
        v-for="(tab, index) in projectTabs" 
        :key="index" 
        @click="switchProject(index)">
        {{ tab }}
      </button>
    </div>

    <!-- Projekt-innehåll -->
    <div
      v-for="(project, pIndex) in projects"
      :key="pIndex"
      :class="['project', { 'current': activeProject === pIndex }]"
    >
      <!-- Inre Tab knappar -->
      <div class="tab-box">
        <button
          v-for="(tab, index) in innerTabs"
          :key="index"
          :class="['tab-btn', { 'active': activeInnerTab[pIndex] === index }]"
          @click="switchInnerTab(pIndex, index)"
        >
          {{ tab }}
        </button>
      </div>

      <!-- Inre Tab-innehåll -->
      <div
        v-for="(content, index) in project.content"
        :key="index"
        :class="['tab-content', { 'active': activeInnerTab[pIndex] === index }]"
      >
        <div class="inner-wrap">
          <div class="text">
            <h3>{{ content.heading }}</h3>
            <p>{{ content.text }}</p>
            
            <h4>
                <a v-if="content.link" :href="content.link" target="_blank" rel="noopener noreferrer">
                  {{ content.link_text }}
                </a>
            </h4>
            <h4>
                <a v-if="content.github" :href="content.github" target="_blank" rel="noopener noreferrer">
                  {{ content.git_text }}
                </a>
            </h4>

           
            
          </div>
          <div class="thumb">
            <img v-if="content.image" :src="content.image" alt="Thumbnail" class="thumbnail" />
          </div>
        </div>
      </div>
    </div>
    
  </section>
</article>
</template>

<script>
import { gsap } from "gsap";

export default {
  name: "SiteLab",
  data() {
    return {
      projectTabs: ["Portfolio sidan", "Gym-sidan", "Barber-sidan", ],
      activeProject: 0,
      activeInnerTab: [0, 0, 0], 
      innerTabs: ["Summary", "What?", "How?", "Why?"],

      projects: [
        {
          content: [
            {
              heading: "Summary",
              text: "Denna Vue-baserade webbapplikation, byggd med HTML, CSS, och JavaScript, är skapad för att presentera mina färdigheter och projekt som webbutvecklare. Med hjälp av GSAP (GreenSock Animation Platform) har jag implementerat smidiga övergångar och animationer, vilket skapar en engagerande och dynamisk användarupplevelse. En av de mest framträdande funktionerna är flik-systemet, där användare enkelt kan navigera mellan olika projekt och utforska detaljerna bakom dem. Varje projekt visas med specifik information om vad det är, hur det byggdes, och varför det utvecklades.",
              image: "/thumb.png",
              git_text: "Länk till github-repo:",
              github: "test.github.se"
            },
            {
              heading: "What",
              text: "Den här sidan fungerar som ett centralt nav för mina utvalda projekt och är utformad för att framhäva mina färdigheter och erfarenheter som webbutvecklare. Genom att visa upp mina arbeten i en interaktiv och visuellt tilltalande miljö, fungerar sidan som ett sätt att marknadsföra mig själv och ge potentiella arbetsgivare eller kunder en tydlig bild av vad jag kan åstadkomma. Sidan hjälper också till att kommunicera mitt arbetssätt, från idé till färdig produkt, och understryker mitt fokus på både estetik och funktionalitet.",
              
            },
            {
              heading: "How",
              text: "Utvecklingen av sidan började med att jag skissade layouten för hand för att snabbt visualisera strukturen och flödet. Därefter skapade jag en mer detaljerad digital prototyp i Figma, där jag kunde experimentera med design, färgscheman och användarflöde. Efter att prototypen var färdig, utvecklade jag en statisk version av sidan för att testa de grundläggande visuella och strukturella elementen. Slutligen integrerade jag funktionaliteten genom att omvandla sidan till en fullfjädrad Vue-applikation, med dynamiskt innehåll och animationer via GSAP.",
              
            },
            {
              heading: "Why",
              text: "Jag valde att bygga denna portfolio med Vue.js eftersom det är ett kraftfullt men samtidigt flexibelt ramverk som gör det enkelt att skapa interaktiva gränssnitt. Vue's komponentbaserade struktur hjälper till att hålla koden organiserad och lätt underhållbar, vilket är viktigt för en växande applikation. GSAP valdes för att skapa avancerade och flytande animationer, vilket förbättrar användarupplevelsen genom att göra navigeringen mer dynamisk och engagerande. Kombinationen av dessa tekniker visar inte bara mina färdigheter inom frontend-utveckling, utan understryker även min förmåga att skapa moderna, användarcentrerade webblösningar. Att använda HTML, CSS och JavaScript som grundläggande byggstenar för applikationen gör den både standardkompatibel och tillgänglig för vidareutveckling.",
              
            },
          ],
        },
        {
          content: [
            {
              heading: "Summary",
              text: "Denna webbplats för ett fiktivt gym skapades som ett experiment för att utforska hur en modern och responsiv gymsida kan se ut, med utgångspunkt i de brister jag upptäckte när jag själv letade efter ett nytt gym. Målet var att skapa en sida som kombinerar uppdaterad design, användarvänlighet och nödvändig information, vilket många existerande gymsidor saknar.",
              image: "/Gym_thumb.png",
              link_text: "Länk till webbplats:",
              link: "https://dynamic-pixie-2a663b.netlify.app/about",
              git_text: "Länk till github-repo:",
              github: "https://github.com/LeRuggedHermit/https---github.com-LeRuggedHermit-XtremeGym_Vue"
            },
            {
              heading: "What",
              text: "Den här webbplatsen är en mockup för ett fiktivt gym, designad för att visa hur en modern och funktionell gymsida kan se ut och fungera. Den innehåller information om gymmet och dess utbud, inklusive olika kampsporter, samt ett bokningsformulär och ett träningsschema för de sporter som erbjuds. Med fokus på att skapa en responsiv och användarvänlig upplevelse fungerar sidan som en prototyp för en gymsida som är både visuellt tilltalande och lättnavigerad.",
              
            },
            {
              heading: "How",
              text: "Processen för att bygga den här gymsidan liknade utvecklingen av min portfolio. Efter att ha skissat layouten på papper, övergick jag till en digital prototyp i Figma för att planera design och användarflöde. Bilder hämtades från Unsplash, medan jag själv designade logotyper och faviconer. Webbplatsen utvecklades först som ett WordPress-tema med PHP, vilket gjorde det möjligt att bygga en dynamisk och lättuppdaterad webbplats med hjälp av ett CMS. Därefter omvandlade jag projektet till en Vue.js-applikation, med GSAP-animationer för övergångar och interaktivitet. Sidan innehåller också ett bokningsformulär och ett träningsschema för de sporter som erbjuds, även om bokningssystemet inte har backend-funktionalitet.",
              
            },
            {
              heading: "Why",
              text: "Jag valde att först bygga webbplatsen som ett WordPress-tema för att testa hur man kan integrera ett användarvänligt CMS i ett gymsammanhang. Detta gjorde det möjligt att skapa en dynamisk och lättuppdaterad sida, något som är viktigt för gym där information ständigt förändras. Efter att ha utforskat WordPress valde jag att vidareutveckla sidan som en Vue.js-applikation, vilket gav mig mer kontroll över funktionalitet och användarupplevelse. Syftet var att lösa de problem jag sett med många befintliga gymsidor – att de var föråldrade och svåra att använda – och skapa en modern, responsiv och användarvänlig lösning.",
              
            },
          ],
        },
        {
          content: [
            {
              heading: "Summary",
              text: "Bob’s Barbershop är en stilfull och interaktiv mockup för en fiktiv barbershop med fokus på både design och användarvänlighet. Den är byggd med React och GSAP för att skapa smidiga animationer och en engagerande upplevelse, där användaren kan interagera med element som en bild-slider och bokningskalender. Sidan kombinerar punkrock-estetik med en modern webbdesign, vilket speglar barberarens unika karaktär och stil, och visar upp en välbalanserad mix av visuella effekter och funktionell design.",
              image: "/barber_thumb.png",
              link_text: "Länk till webbplats:",
              link: "https://chimerical-starburst-77543e.netlify.app/",
              git_text: "Länk till github-repo:",
              github: "https://github.com/LeRuggedHermit/BobsBarber_react"
            },
            {
              heading: "What",
              text: "Denna webbplats är en mockup för en fiktiv barberare som heter 'Bob's Barbershop.' Målet var att skapa en visuellt intressant och estetiskt tilltalande sida, samtidigt som användarvänligheten bevarades. Webbplatsen innehåller ett anpassat bokningssystem och kontaktformulär, samt en egendesignad bild-slider som fungerar med musinteraktion",
              
            },
            {
              heading: "How",
              text: "Webbplatsen byggdes med React och GSAP (GreenSock Animation Platform) för att skapa smidiga animationer och interaktiva element. Jag designade alla logotyper och faviconer själv, och använde Unsplash för bildmaterial. Det här projektet var också mitt första större arbete med GSAP, där jag experimenterade med olika animationstekniker. Jag skapade en specialbyggd bokningskalender och en bild-slider, där musinteraktion används för att manipulera bilders positioner i realtid. Detta var också ett test på hur GSAP och React kan integreras för att skapa en dynamisk och engagerande användarupplevelse.",
              
            },
            {
              heading: "Why",
              text: "Jag ville skapa en sida som utforskar estetisk design för en barberarverksamhet utan att kompromissa med användarupplevelsen. Detta projekt var ett tillfälle att utforska och finslipa mina kunskaper i GSAP och hur jag kan använda det i kombination med React. Syftet var att leverera en visuellt tilltalande och tekniskt utmanande sida, som visar upp både design- och animationsförmågor. Samtidigt ville jag skapa en lättnavigerad och funktionell sida som speglar den rockiga och rebelliska stilen hos den fiktiva barbershopen.",
              
            },
          ],
        },
      ],
    };
  },
  methods: {
  
  switchProject(index) {
    if (this.activeProject !== index) {
      this.animateSwitch(this.activeProject, index); 
      this.activeProject = index;
      
      this.activeInnerTab[index] = 0;
    }
  },

 
  switchInnerTab(projectIndex, tabIndex) {
    if (this.activeInnerTab[projectIndex] !== tabIndex) {
      this.animateInnerTabSwitch(
        this.activeInnerTab[projectIndex],
        tabIndex,
        projectIndex
      ); 
      this.activeInnerTab[projectIndex] = tabIndex;
    }
  },

  
  animateSwitch(oldIndex, newIndex) {
    const oldTab = document.querySelectorAll(".project")[oldIndex];
    const newTab = document.querySelectorAll(".project")[newIndex];

    gsap.to(oldTab, { autoAlpha: 0, y: 50, duration: 0.5 });
    gsap.fromTo(
      newTab,
      { autoAlpha: 0, y: 50 },
      { autoAlpha: 1, y: 0, duration: 0.5 }
    );
  },

 
  animateInnerTabSwitch(oldTabIndex, newTabIndex, projectIndex) {
    const oldContent = document.querySelectorAll(
      `.project:nth-child(${projectIndex + 1}) .tab-content`
    )[oldTabIndex];
    const newContent = document.querySelectorAll(
      `.project:nth-child(${projectIndex + 1}) .tab-content`
    )[newTabIndex];

    gsap.to(oldContent, { autoAlpha: 0, y: 20, duration: 0.5 });
    gsap.fromTo(
      newContent,
      { autoAlpha: 0, y: 20 },
      { autoAlpha: 1, y: 0, duration: 0.5 }
    );
  },
},
  mounted() {
    gsap.fromTo(
      document.querySelectorAll(".project")[0],
      { autoAlpha: 0, y: 50 },
      { autoAlpha: 1, y: 0, duration: 0.5 }
    );
  },
};
</script>


<style scoped>
/*Andra artikeln:*/

.content-container-2 {
  width: 80%;
  padding: 3rem;
}

.lab-heading {
  margin-bottom: 10rem;
  width: 100%;
  text-align: center;
}

.lab-heading h1 {
  font-size: 82.26px;
}

.lab-heading p {
  font-size: 19.42px;
  font-weight: 500;
}

.content {
  width: 100%;
  display: flex;
  justify-content: space-evenly;
  gap: 4vmin;
}

.project-tab {
  width: 30%;
  margin-bottom: 5rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  align-content: center;
  gap: 4vmin;
}

.p-tab {
  width: 160px;
  height: 40px;
  border: none;
  background-color: #b7b4d1;
  cursor: pointer;
  transition: background-color 0.3s ease-in-out, border-radius 0.3s ease-in-out;
}

.p-tab:hover {
  background-color: rgb(126, 217, 174);
  border-radius: 25px;
}

.project {
  display: none;
  width: 100%;
  height: fit-content;
}

.current {
  display: block;
  font-weight: 600;
}

.tab-box {
  width: 100%;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  border-bottom: solid black 2px;
}

.tab-btn {
  font-family: "Barlow Semi Condensed", sans-serif;
  font-size: 18px;
  font-weight: 600;
  border: none;
  outline: none;
  background-color: rgb(0, 0, 0);
  color: white;
  width: 100px;
  height: 100px;
  margin-top: 1vmin;
  margin-bottom: 1vmin;
  cursor: pointer;
  transition: background-color 0.3s ease-in-out;
}

.tab-btn:hover {
  background-color: rgb(217, 191, 126);
  color: black;
}

.tab-content {
  display: none;
}

.active {
  display: block;
}

.inner-wrap {
  display: flex;
  flex-direction: row;
  margin-top: 1rem;
  gap: 2vmin;
}

.text {
  width: 60%;
  font-weight: 300;
}


.thumb {
  margin-right: 1rem;
  width: 50%;
  height: fit-content;
  
}

.thumbnail {
  width: 100%;
  aspect-ratio: 2/1;
  object-fit: cover;
  border: solid black 1px;
}




/* MEDIA QUERIES: */

@media screen and (max-width: 600px){
   /*Andra artikeln: */

   .content-container-2 {
    width: 90%;
    padding: 1rem;
  }

  .content {
    width: 100%;
    display: flex;
    flex-direction: column;
    gap: 4vmin;
    border: solid black 1px;
  }

  .lab-heading h1 {
    font-size: 53px;
  }

  .project-tab {
    width: 100%;
    flex-direction: row;
  }

  .p-tab {
    height: 100px;
    background-color: #2c285a;
    color: white;
  }

  .tab-box {
    gap: 1vmin;
    margin-bottom: 0;
  }

  .tab-btn {
    border-radius: 0px;
    margin-bottom: none;
    height: 100px;
    border: solid black 1px;
    gap: 1vmin;
  }

  .inner-wrap {
    flex-direction: column-reverse;
  }

  .thumb {
    width: 100%;
    height: fit-content;
    border: none;
    border-bottom: solid rgb(94, 94, 94) 2px;
  }

  .text {
    width: 100%;
    font-weight: 300;
    display: flex;
    flex-direction: column;
    align-items: center;
    align-content: center;
    height: fit-content;
  }

  .text p {
    width: 80%;
  }
}
</style>