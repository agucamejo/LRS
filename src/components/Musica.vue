<template>
    <section class="py-16">
      <div class="max-w-screen-lg mx-auto px-4 md:px-8">
        <div class="max-w-md">
            <h1 class="text-white text-2xl font-extrabold sm:text-3xl">MÚSICA</h1>
        </div>
        <div class="flex justify-center mt-16">
            <iframe style="border-radius:12px" src="https://open.spotify.com/embed/playlist/54TVXLm7QNxDUA898ZciL4?utm_source=generator&theme=0" width="100%" height="420" frameBorder="0" allowfullscreen="true" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
        </div>
        <!-- <div id="twitch-embed"></div> -->
      </div>
    </section>
</template>


<!-- <script>
export default {
  mounted() {
    // Create a script element
    const script = document.createElement('script');

    // Set the source of the script to the Twitch embed script
    script.src = 'https://player.twitch.tv/js/embed/v1.js';

    // Append the script element to the document's head
    document.head.appendChild(script);

    // Define the Twitch player creation function
    script.onload = () => {
      new Twitch.Player("twitch-embed", {
        channel: "tukitag"
      });
    };
  }
};
</script> -->