<template>
  <section class="pb-16">
    <div class="max-w-screen-lg mx-auto px-4 md:px-8">
      <div>
        <h3 class="text-yellow-600 text-4xl font-semibold text-center max-md:text-3xl">Próximo evento</h3>
        <h2 class="text-green-500 text-8xl font-bold text-center max-sm:text-4xl mt-12">PREMIOS LRS</h2>
        <div class="flex flex-col items-center">
          <div class="flex justify-center items-center gap-10 mb-12 mt-10 max-md:gap-2">
            <div class="time-box">
              <span id="days" class="time-value"></span>
              <span class="time-label">días</span>
            </div>
            <div class="time-box">
              <span id="hours" class="time-value"></span>
              <span class="time-label">horas</span>
            </div>
            <div class="time-box">
              <span id="minutes" class="time-value"></span>
              <span class="time-label">minutos</span>
            </div>
            <div class="time-box">
              <span id="seconds" class="time-value"></span>
              <span class="time-label">segundos</span>
            </div>
          </div>
          <iframe src="https://www.youtube.com/embed/Vd4OETAjawk?si=yFEiNUz3pwbU9cAo" 
                  title="Video de los premios LRS" 
                  frameborder="0" 
                  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                  referrerpolicy="strict-origin-when-cross-origin" 
                  allowfullscreen>
          </iframe>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  mounted() {
    const targetDate = new Date("2024-12-20T21:00:00").getTime();
    
    const updateCountdown = () => {
      const now = new Date().getTime();
      const difference = targetDate - now;

      if (difference <= 0) {
        document.getElementById("days").textContent = "00";
        document.getElementById("hours").textContent = "00";
        document.getElementById("minutes").textContent = "00";
        document.getElementById("seconds").textContent = "00";
        return;
      }

      const days = String(Math.floor(difference / (1000 * 60 * 60 * 24))).padStart(2, "0");
      const hours = String(Math.floor((difference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60))).padStart(2, "0");
      const minutes = String(Math.floor((difference % (1000 * 60 * 60)) / (1000 * 60))).padStart(2, "0");
      const seconds = String(Math.floor((difference % (1000 * 60)) / 1000)).padStart(2, "0");

      document.getElementById("days").textContent = days;
      document.getElementById("hours").textContent = hours;
      document.getElementById("minutes").textContent = minutes;
      document.getElementById("seconds").textContent = seconds;
    };

    updateCountdown();
    setInterval(updateCountdown, 1000);
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Orbitron:wght@700&display=swap");

.time-box {
  display: flex;
  flex-direction: column;
  align-items: center;
  color: #bef550; 
}

.time-value {
  font-family: "Orbitron", sans-serif;
  font-size: 3rem;
  text-align: center;
}

.time-label {
  font-size: 1rem;
  text-transform: uppercase;
}
</style>
