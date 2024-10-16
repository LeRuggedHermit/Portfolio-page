<template>
     <!--Första artikeln: presentation: -->
     <article class="introduction-container">
        <div class="wrap-container">
            <section class="introduction">
              <div class="introduction-box" id="top-box">
                <div class="introduction-content">
                <h1>
                  Utbildad Fullstacksutvecklare.
                </h1>
                <p>
                  Hej! Jag heter Simon Brandtman och är en fullstackutvecklare med en passion för att skapa effektiva och moderna webbapplikationer.</p>
                   <p>
                    Jag tog nyligen examen inom webbprogrammering och arbetar med både front-end och back-end, där jag utnyttjar mina kunskaper inom flera webbteknologier.
                </p>
                <p>
                  Explore my projects and learn more about me here!
                </p>
              </div>
              </div>
            </section>
            <section class="content-box">
              <div class="text-box">
                <h1>Trevligt att råkas!</h1>
                <p>Tack för att du besöker min portfolio. </p>
                <p>Jag motiveras av utmaningen att skapa intuitiva UI/UX-upplevelser som gör webbapplikationer både funktionella och behagliga att använda.</p>
                <p>Utforska mina projekt för att se hur jag kombinerar design och kod för att skapa sömlösa användarupplevelser.</p>
                <p>Om du söker en utvecklare som är engagerad i att skapa moderna och engagerande gränssnitt, skulle jag gärna vilja höras av och diskutera hur vi kan samarbeta!</p>
              </div>
              <div class="link-box">         
                  <img src="../assets/PB.png" alt="portrait" id="pic">
                <button id="contact_btn">Get in touch!</button>
                <div class="button-box">
                  <a href="#" class="social-btn"><img src="../assets/linkedin-svgrepo-com(1).svg" alt="LinkedIn"></a>
                  <a href="#" class="social-btn"><img src="../assets/github-svgrepo-com.svg" alt="Github"></a>
                  <a href="#" class="social-btn"><img src="../assets/mail-svgrepo-com.svg" alt="email"></a>
                </div>
              </div>
            </section>
        </div>
          </article>
</template>

<script>
export default{
    name: 'SiteIntroduction',

}
</script>

<style>
/*första artikeln*/

.introduction-container {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  align-content: center;
}

.wrap-container {
  width: 90%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin-bottom: 5rem;
}

.introduction {
  width: 25%;
  height: 100%;
}

.introduction-box {
  width: 100%;
  aspect-ratio: 1;
  background-color: #d9d9d9;
  padding: 2rem;
  clip-path: inset(0 10px round 15% 0);
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  align-content: center;
}

.introduction-content {
  background-color: white;
  width: 80%;
  aspect-ratio: 1;
  clip-path: inset(0 10px round 15% 0);
  padding: 1.5rem;
}

#top-box {
  margin-bottom: 6rem;
}

.content-box {
  width: 700px;
  display: flex;
  flex-direction: row;
  background-color: #d9d9d9;
}

.info-box p {
  font-weight: 200;
}

.text-box {
  width: 50%;
  padding: 1rem;
}

.text-box h1 {
  font-size: 50.9px;
  text-align: center;
}

#pic {
  width: 200px;
  aspect-ratio: 1;
  border-radius: 50%;
  margin-top: 1rem;
}

.link-box {
  padding: 2rem;
  width: 50%;
  display: flex;
  flex-direction: column;
  align-items: center;
  align-content: center;
}

#contact_btn {
  margin-top: 2rem;
  width: 200px;
  background-color: black;
  height: 24px;
  border-radius: 25px;
  color: white;
  font-family: "Urbanist", sans-serif;
  border: none;
  cursor: pointer;
}

.button-box {
  width: 300px;
  border-radius: 50px;
  height: 60px;
  background-color: #d9d9d9;
  display: flex;
  flex-direction: row;
  gap: 2vmin;
  align-items: center;
  align-content: center;
  justify-content: space-evenly;
  margin-top: 2rem;
}

.social-btn {
  position: relative;
  width: 50px;
  aspect-ratio: 1;
  border-radius: 50%;
  background-color: rgb(255, 255, 255);
  box-shadow: 2px 3px 4px 1px rgb(186, 186, 186);
  cursor: pointer;
  text-align: center;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  align-content: center;
}

.social-btn img {
  width: 50px;
  aspect-ratio: 1;
}

/*------------------Media queries: ------------------------------- */
/*För väldigt små skärmar */
@media screen and (max-width: 400px){
.wrap-container {
    flex-direction: column;

    align-items: center;
    align-content: center;
  }

  .introduction {
    width: 100%;
    aspect-ratio: 1;
  }

  .content-box {
    width: 300px;
    flex-direction: column;
    align-items: center;
  }

  .text-box {
    width: 80%;
    padding: 1rem;
  }

  #pic {
    width: 200px;
  }

  #contact_btn {
    width: 80%;
    height: 50px;
    font-size: larger;
  }

  .button-box {
    width: 300px;
    margin-top: 3rem;
  }

  .introduction {
    display: none;
  }}

  /*För små skärmar */
  @media screen and (min-width: 401px) and (max-width: 640px){

    .wrap-container {
    flex-direction: column;

    align-items: center;
    align-content: center;
  }

  .content-box {
    width: 300px;
    flex-direction: column;
    align-items: center;
  }

  .text-box {
    width: 80%;
    padding: 1rem;
  }

  #pic {
    width: 200px;
  }

  #contact_btn {
    width: 80%;
    height: 50px;
    font-size: larger;
  }

  .button-box {
    width: 300px;
    margin-top: 3rem;
  }

  .introduction {
    display: none;

  }

  .social-btn {
    width:70px;
    aspect-ratio: 1;
  }

  .social-btn img {
  width: 70px;
  aspect-ratio: 1;
}
}

  /* Får medium skärmar: */
  @media screen and (min-width:641px) and (max-width: 860px){

    .wrap-container{
      flex-direction: column-reverse;
      align-items: center;
      align-content: center;
    }

    .content-box {
    width: 600px;
    flex-direction: column;
    align-items: center;
  }

  .introduction{
    width: 600px;
    display: flex;
    flex-direction: column;
    align-content: center;
    align-items: center;
  }

  .introduction-box{
    margin-top: 2rem;
    width: 50%;
  }

  }

  /* för medium-stora skärmar */
  @media screen and (min-width: 861px) and (max-width: 1130px){

    .wrap-container{
      flex-direction: column-reverse;
      align-items: center;
      align-content: center;
    }

    .content-box {
    width: 800px;
    flex-direction: column;
    align-items: center;
  }

  .introduction{
    width: 800px;
    display: flex;
    flex-direction: column;
    align-content: center;
    align-items: center;
  }

  .introduction-box{
    margin-top: 2rem;
    width: 50%;
  }
  } 

</style>