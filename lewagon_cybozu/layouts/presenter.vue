/*
  ---
  layout: presenter
  eventLogo: 'https://img2.storyblok.com/352x0/f/84560/2388x414/23d8eb4b8d/vue-amsterdam-with-name.png'
  eventUrl: 'https://vuejs.amsterdam/'
  twitter: '@alvaro_code'
  twitterUrl: 'https://twitter.com/alvaro_code'
  presenterImage: 'https://res.cloudinary.com/alvarosaburido/image/upload/v1622370075/as-portfolio/alvaro_saburido.jpg'
  ---

  # Alvaro Saburido Rodriguez

  Senior Front-end Engineer at <fancy-link  href="https://bcn.porsche.digital/en/" favicon="https://www.google.com/s2/favicons?domain=porsche.com" >Porsche Digital</fancy-link>

  - Dev Advocate
  - I often write at <fancy-link href="https://dev.to/alvarosaburido">@alvarosaburido</fancy-link>
  - Portfolio <fancy-link href="https://alvarosaburido.dev">alvarosaburido.dev</fancy-link>
  - Say hi at <fancy-link href="https://twitter.com/alvaro_code">@alvaro_code</fancy-link>

  ---
*/

<script setup lang="ts">
import { defineProps, defineComponent } from "vue";
import Default from "./default.vue";

const components = defineComponent({ Default });
const props = defineProps({
  eventLogo: {
    type: String,
  },
  eventUrl: {
    type: String,
  },
  twitter: {
    type: String,
  },
  twitterUrl: {
    type: String,
  },
  presenterImage: {
    type: String,
  },
});
</script>

<template>
  <default
    class="presenter"
    :logo-header="logoHeader"
    :event-logo="eventLogo"
    :event-url="eventUrl"
    :twitter="twitter"
    :twitter-url="twitterUrl"
  >
    <div class="flex items-center">
      <figure class="w-1/2 px-12">
        <img
          :src="presenterImage"
          class="
            rounded-full
            object-cover
            h-80
            w-80
            border border-8 border-secondary-400
          "
        />
      </figure>
      <div class="w-1/2">
        <slot />
      </div>
    </div>
  </default>
</template>