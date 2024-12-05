<template>
  <div class="hero-section">
    <div id="videoContainer">
      <video id="videoBackground" autoplay="true" muted="true" loop="true">
        <source src="../assets/video/video-background.mp4">
      </video>
    </div>
    <div class="content max-w-screen-lg min-h-[calc(100vh-120px)] pt-[110px] flex flex-col gap-8 items-center justify-center mx-auto px-4 md:px-8">
      <div class="w-full">
        <h1 class="text-6xl text-[#fe3838] sm:text-[10rem] text-center lacquer-regular">
          LRS GANG
        </h1>
      </div>
      <div class="flex flex-col items-center sm:mt-[2rem] gap-4">
        <h3 class="text-yellow-600 text-4xl max-md:text-3xl font-semibold">Nuestros valores</h3>
        <div class="flex flex-col items-center">
          <p class="text-white text-center text-2xl max-md:text-lg my-2 w-4/5 font-thin">
            La honestidad, la lealtad y el respeto son la clave. Hablamos de frente, estamos juntos en las buenas y en las malas, y nos tratamos con el respeto que cada uno merece. 
          </p>
          <p class="text-white text-center text-3xl max-md:text-lg mt-5 w-5/5 ">¡Bienvenido a la familia LRS y sentite libre de ser vos mismo! 💜</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Lacquer&display=swap');

#videoContainer {
  top: 0;
  left: 0;
  width: 100vw;
  width: 100%;
  height: 100vh;
  text-align: center;
  overflow: hidden;
  z-index: -100;
  position: fixed;
}

#videoBackground {
  width: inherit;
  height: inherit;
  -o-filter: blur(8px) brightness(50%);
  filter: blur(8px) brightness(50%);
  -o-object-fit: cover;
  object-fit: cover;
  transform: scale(1.1);
}

.lacquer-regular {
  font-family: "Lacquer", system-ui;
  font-weight: 400;
  font-style: normal;
}

.hero-section {
  position: relative;
  min-height: calc(100vh); 
  top: -120px; 
  overflow: hidden; 
}

.hero-section::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-position: center;
  filter: grayscale(100%); 
  z-index: 1; 
}

.hero-section{
  mask-image: linear-gradient(to bottom, black 75%, transparent 100%);
  -webkit-mask-image: linear-gradient(to bottom, black 75%, transparent 100%);
}

.hero-section::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5); 
  z-index: 2; 
}

.content-title {
  filter: drop-shadow(4px 6px 12px green);
  position: relative;
  z-index: 3;
}

.content {
  filter: drop-shadow(4px 6px 8px black);
  position: relative;
  z-index: 3;
}
</style>
