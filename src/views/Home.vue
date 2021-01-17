<template>
  <div class="home">
    <div class="info">
      <img class="photo" src="../assets/borja-black.png" alt="This is me">
      <p class="text name">Borja Rodrigo</p>
      <p class="text job">Frontend Developer</p>
      <div class="social">
        <a href="https://gitlab.voicemod.tech/borja.rodrigo" target="_blank" rel="noopener noreferrer">
          <i class="fab fa-gitlab"></i>
        </a>
        <a href="https://github.com/zordycor" target="_blank" rel="noopener noreferrer">
          <i class="fab fa-github"></i>
        </a>
        <a href="https://www.instagram.com/zordycor/" target="_blank" rel="noopener noreferrer">
          <i class="fab fa-instagram"></i>
        </a>
        <a href="mailto:zordycorak@gmail.com" target="_blank" rel="noopener noreferrer">
          <i class="far fa-envelope"></i>
        </a>
      </div>
      <div class="experience">
        <p class="text">In 2018 I finished my Degree on CE at the UPV <a :href="`${publicPath}TFG_Tapas.pdf`" download="TFG Borja Rodrigo">(<u>This</u> is my final project, it's a webpage)</a>.</p>
        <p class="text">Then, the same year, I joined Epigram Technologies, my first job as a web developer!</p>
        <p class="text">After one and a half years I joined Jeff as a Junior FE Developer. We are on 2019.</p>
        <p class="text">Like eight months passed and the coronavirus arrived! I got fired. So in 2020 I joined Voicemod.</p>
        <p class="text">I think that's all so far.</p>
      </div>
      <a class="cv text" :href="`${publicPath}CV_Borja.pdf`" download="CV Borja">
        <p>Here's my CV</p><i class="far fa-save"></i>
      </a>
      <p class="recomendations text">
        Here should be reommendations of my colleagues. Soon...
      </p>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({ publicPath: process.env.BASE_URL })
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100;400;600&display=swap');

* {
  font-family: 'Montserrat', sans-serif;
  font-size: 15px;
}

a:visited,
a:link,
a:hover,
a:active {
  color: black;
  text-decoration-line: none;
}


.home {
  margin: 0 auto;
  max-width: 700px;
}

.info {
  height: 100%;
  margin: 40px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.photo {
  border-radius: 50%;
  max-width: 200px;
}

.text {
  margin-top: 20px;
  width: 100%;
}

.name,
.job {
  text-align: center;
}

.job {
  margin-bottom: 20px;
  font-weight: 600;
}

.social {
  display: flex;
  margin-bottom: 20px;
}

.fab,
.far {
  font-size: 35px;
  margin: 0 15px;
}

.cv {
  width: 100%;
  display: flex;
  align-items: baseline;
}

.cv .far {
   font-size: 18px;
 }
</style>
