<template>
  <!-- Simple header with scrollable tabs. -->
<div class="mdl-layout mdl-js-layout mdl-layout--fixed-header mdl-app mdl-color-text--grey-700">
  <header class="mdl-layout__header mdl-layout__header--scroll">
  <div class="mdl-layout--large-screen-only mdl-layout__header-row"></div>
    <div class="mdl-layout__header-row">
      <!-- Title -->
      <h3 class="mdl-layout--large-screen-only">{{title}}</h3>
      <span class="mdl-layout-title mdl-layout--small-screen-only">{{title}}</span>
    </div>
    <div class="mdl-layout--large-screen-only mdl-layout__header-row"></div>
    <!-- Tabs -->
    <div class="mdl-layout__tab-bar mdl-js-ripple-effect">
      <a href="#intro-tab" class="mdl-layout__tab is-active">Introdução</a>
      <a href="#virtualization-tab" class="mdl-layout__tab">Virtualiação</a>
      <a href="#challenges-tab" class="mdl-layout__tab">Desafios</a>
      <a href="#sdn-tab" class="mdl-layout__tab">SDN</a>
      <a href="#bibliography-tab" class="mdl-layout__tab">Bibliografia</a>
    </div>
  </header>
  
  <main class="mdl-layout__content">
    <intro-tab></intro-tab>
    <virtualization-tab></virtualization-tab>
    <challenges-tab></challenges-tab>
    <sdn-tab></sdn-tab>
    <bibliography-tab></bibliography-tab>
    <authorship-section></authorship-section>
  	<home-footer></home-footer>
  </main>
</div>
</template>

<script>
import IntroTab from './IntroTab.vue'
import HomeFooter from './HomeFooter/HomeFooter.vue'
import BibliographyTab from './BibliographyTab.vue'
import VirtualizationTab from './VirtualizationTab/VirtualizationTab.vue'
import ChallengesTab from './ChallengesTab/ChallengesTab.vue'
import SdnTab from './SDNTab/SDNTab.vue'
import AuthorshipSection from './AuthorshipSection.vue'

export default {
  name: 'home',
  components: {
    IntroTab, BibliographyTab, HomeFooter, AuthorshipSection, VirtualizationTab, ChallengesTab, SdnTab
  },
  data () {
    return {
      title: 'NFV'
    }
  }
}
</script>

<style lang="sass">
  .mdl-app {
    section {
      &.section--center {
        max-width: 860px;
        margin: auto;
      }
    }

    .mdl-layout__tab-panel {
      padding: 8px;
      padding-top: 48px;
    }
  }
</style>
