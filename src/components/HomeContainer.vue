<template>
  <div class="container">
    <ContentsHero />
    <ContentsSelfintroduction />
    <ContentsBio />
    <ContentsSkills />
    <ContentsWorks />
    <ContentsNews />
    <ContentsContact />
  </div>
</template>

<script>
import ContentsHero from './contents/ContentsHero.vue'
import ContentsSelfintroduction from './contents/ContentsSelfintroduction.vue'
import ContentsBio from './contents/ContentsBio.vue'
import ContentsSkills from './contents/ContentsSkills.vue'
import ContentsWorks from './contents/ContentsWorks.vue'
import ContentsNews from './contents/ContentsNews.vue'
import ContentsContact from './contents/ContentsContact.vue'


export default {
  name: 'TheContainer',
  components: {
    ContentsHero,
    ContentsSelfintroduction,
    ContentsBio,
    ContentsSkills,
    ContentsWorks,
    ContentsNews,
    ContentsContact
  }
}
</script>

<style lang="scss" scoped>
@import "../styles/_variables.scss";
@import "../styles/_mixins.scss";

.container {
  width: 90%;
  height: 90%;
  position: absolute;
  position: fixed;
  overflow: auto;
  top: 6%;
  right: 5%;
  border-radius: 0px;
    
  @include box-shadow_inset;
}

.contents {  
  @include contents_global;
}


/*
Responsive
================================================ */
@media (min-width: calc(7000px / 9)) {
  .container {
    @include responsive_container_width;
  }
}

@media (max-height: 850px) {
  .container {
    @include responsive_container_height;
  }
}

</style>