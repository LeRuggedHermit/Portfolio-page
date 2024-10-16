<template>
              <!--About-artikel: -->
              <article class="about" id="about">
    <section class="main-text">
      <h1>So about me...</h1>
      <h4>I hope I’ve piqued your interest! Allow me to tell you more about myself.</h4>
      <p>I’m a full-stack developer with a degree in Web Development from Mid Sweden University, Sundsvall. </p>
      <p>My studies have given me the skills to design and develop a wide range of websites and applications, with knowledge spanning both front-end and back-end development.</p>
      <p>This knowledge is not limited to one single area such as front-end or back-end, but encompasses all areas of design and development.</p>
      <p>I am familiar with most modern technologies that are used today for creating for the web.</p>
      <p>I’m always eager to learn more, continuously expanding my skillset to stay up-to-date with the latest trends and technologies.</p>
      <h4>If you think I could be a great fit for your team, don’t hesitate to contact me!</h4>
    <h4>Also, please check out my CV  <router-link to="/about">here</router-link></h4>
    </section>
    <section class="puffs">
      <div class="puff">
        <h3>Hör av dig via mail: </h3>
        <a href="mailto:">brandtman@hotmail.se</a>
        <img src="../assets/mail-svgrepo-com.svg" alt="mail-icon">
      </div>
      <div class="puff">
        <h3>Kontakta mig på LinkedIn</h3>
        <a href="https://www.linkedin.com/in/simon-brandtman-4199b22b8/">Simon Brandtman - LinkedIn</a>
        <img src="../assets/linkedin-svgrepo-com(1).svg" alt="linkedin-logo">
      </div>
    </section>
        </article>
</template>


<script>
export default{
    name: 'AboutContent',
}
</script>

<style scoped>
/*Sista segmentet: */

.about {
  margin-top: 10rem;
  margin-bottom: 8rem;
  width: 80%;
  display: flex;
  flex-direction: row;
  gap: 4vmin;
}

.main-text {
  width: 70%;
  padding-bottom: 2vmin;
  padding-left: 4vmin;
  padding-right: 4vmin;
  background-color: #dfb5a9;
}

.main-text h1 {
  font-size: 82.26px;
}

.main-text h4 {
  font-size: 19.42px;
}

.puffs {
  width: 30%;
}

.puff {
  width: 100%;
  background-color: #2c285a;
  color: white;
  height: 10rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  align-content: center;
  margin-bottom: 1rem;
}

.puff a {
  color: white;
}

.puff img {
  width: 50px;
  aspect-ratio: 1;
  background-color: white;
  margin-top: 10px;
  border-radius: 50%;
  object-fit: cover;
  border: solid white 2px;
}


/*------------------------------MEDIA QUERIES:  -----------------------*/
/*För väldigt små skärmar*/
@media screen and (max-width: 400px){
  .about {
    flex-direction: column;
    align-items: center;
    align-content: center;
  }

  .main-text {
    width: 90%;
  }

  .puffs {
    width: 100%;
  }

  .main-text h1{
    font-size: 40px;
  }
}



/*För små och mellan-små skärmar*/
@media screen and (min-width: 401px) and (max-width: 840px){
  .about {
    flex-direction: column;
    align-items: center;
    align-content: center;
  }

  .main-text {
    width: 90%;
  }

  .puffs {
    width: 100%;
  }

  .main-text h1{
    font-size: 40px;
  }
}


</style>