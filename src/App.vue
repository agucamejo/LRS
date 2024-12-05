<script setup>
import Navbar from './components/Navbar.vue';
import Premios from './components/Premios.vue';
// import Musica from './components/Musica.vue';
import Comunidad from './components/Comunidad.vue';
import Evento from './components/Evento.vue';
import Footer from './components/Footer.vue';
import Hero from './components/Hero.vue';

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
  });
};

window.addEventListener('scroll', () => {
  const irArribaElement = document.querySelector('.ir-arriba');
  if (irArribaElement) {
    if (window.scrollY > 0) {
      irArribaElement.style.display = 'block';
    } else {
      irArribaElement.style.display = 'none';
    }
  }
});

</script>

<template>
  <header>
    <Navbar />
  </header>
  <main>
    <Hero />
    <!-- <Comunidad id="comunidad" /> -->
    <Evento id="evento" />
    <Premios id="premios" />
    <Footer id="footer" />
    <!-- <Musica id="musica" /> -->
    <span class="ir-arriba" @click="scrollToTop">
      <svg width="24" height="24" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
        <path fill="currentColor" fill-rule="evenodd" d="M10.103 7.222c3.447 3.468 5.744 5.764 6.89 6.887c.198.185.539.56 1.046.07c.339-.327.325-.685-.039-1.073l-7.444-7.43a.638.638 0 0 0-.455-.176a.702.702 0 0 0-.472.176l-7.453 7.635c-.241.388-.231.715.03.98c.26.265.577.28.95.043z"/>
      </svg>
    </span>
  </main>
</template>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Parkinsans:wght@300..800&display=swap');

.ir-arriba {
	display:none;
	padding:20px;
	background:#024959;
	font-size:20px;
	color:#fff;
	cursor:pointer;
	position: fixed;
	bottom:20px;
	right:20px;
}

body{
  background-color: #101010;
  font-family: "Parkinsans", sans-serif;
  font-optical-sizing: auto;
  font-style: normal;
}
</style>

