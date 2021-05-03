<template>
  <div class="w-full h-full">
    <headline text="Ferienwohnung" />
    <content-section title="Schlafgelegenheiten">
      <template #content>
        <info-card icon="Icon" title="Schlafzimmer 1" details="2 Betten" />
      </template>
    </content-section>
    <content-section title="Ausstattung">
      <template #content> <info-list :items="Features" /> </template>
    </content-section>
  </div>
</template>

<script setup>
import Headline from './components/Typography/Headline.vue'
import InfoCard from './components/InfoCard.vue'
import ContentSection from './components/ContentSection.vue'
import InfoList from './components/InfoList.vue'
import Features from './assets/features.json'
</script>
