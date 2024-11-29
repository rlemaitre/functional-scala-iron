<script setup lang="ts">
import { subtitles } from './subtitles'
import { isEnabled} from "./logic/subtitle";
import SlidesSubtitle from "./components/SlidesSubtitle.vue";

</script>
<template>
  <footer :class="{'with-subtitles': isEnabled}">
    <div class="ledger-logo"></div>
    <div class="conference-logo"></div>
    <LightOrDark>
      <template #light>
        <img src="/images/ledger-light.svg" width="75" class="ledger-logo absolute bottom-13 left-3">
        <img src="/images/conference-light.png" width="150" class="conf-logo absolute bottom-9 right-3">
      </template>
      <template #dark>
        <img src="/images/ledger-dark.svg" width="75" class="ledger-logo absolute bottom-13 left-3">
        <img src="/images/conference-dark.png" width="150" class="conf-logo absolute  bottom-9 right-3">
      </template>
    </LightOrDark>
    <slides-subtitle :subtitles="subtitles" />
  </footer>
</template>
