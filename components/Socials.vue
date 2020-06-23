<template>
  <section>
    <div class="social" v-for="(social, index) in socials" :key="index">
      <a :href="social.url"
        ><img :src="social.iconSrc" :alt="social.name" width="36"
      /></a>
    </div>
  </section>
</template>

<script>
import instagram from "~/assets/img/social/instagram.svg";
import facebook from "~/assets/img/social/facebook.svg";
import bandcamp from "~/assets/img/social/bandcamp.svg";
import spotify from "~/assets/img/social/spotify.svg";
import youtube from "~/assets/img/social/youtube.svg";

export default {
  data() {
    return {
      socials: [
        {
          name: "Instagram",
          url: "https://www.instagram.com/code.lisa/",
          iconSrc: instagram,
        },
        {
          name: "Facebook",
          url: "https://www.facebook.com/codelisaband/",
          iconSrc: facebook,
        },
        {
            name: "Youtube",
            url: "https://www.youtube.com/channel/UCUs1NodAaUIATiqvnspHbhQ",
            iconSrc: youtube,
        },
        {
          name: "Spotify",
          url: "https://open.spotify.com/artist/5TXeiIkDzq9fSMVJZqPuJ0",
          iconSrc: spotify,
        },
        {
          name: "Bandcamp",
          url: "https://codelisa.bandcamp.com/",
          iconSrc: bandcamp,
        },
      ],
    };
  },
};
</script>

<style scoped>
section {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 1rem;
}
.social {
  padding: 0.5rem;
  animation: 3s appear;
}
.social:hover {
  filter: brightness(90%);
}
@keyframes appear {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>