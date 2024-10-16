<script setup>
import SiteIntroduction from '../components/Introduction.vue'
import SiteLab from '../components/Lab.vue'
import siteBanner_2 from '../components/Marquis.vue'
import AboutContent from '../components/About.vue'
</script>

<template>
  <main>
<SiteIntroduction/>
<siteBanner_2 />
<SiteLab />
<AboutContent/>
  </main>
</template>


<style scoped>
main {
  margin-top: 10rem;
  width: 100%;
  font-family: "Barlow Semi Condensed", sans-serif;
  display: flex;
  flex-direction: column;
  align-items: center;
  align-content: center;
}
</style>