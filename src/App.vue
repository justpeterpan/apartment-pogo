<template>
  <div class="w-full h-full">
    <Section title="Schlafgelegenheiten">
      <template #content>
        <InfoCard icon="Icon" title="Schlafzimmer 1" details="2 Betten" />
      </template>
    </Section>
    <Section title="Ausstattung">
      <template #content>
        <InfoListItem icon="icon" text="TV" />
        <InfoListItem icon="icon" text="TV" />
      </template>
    </Section>
  </div>
</template>

<script setup>
import InfoCard from './components/InfoCard.vue'
import Section from './components/Section.vue'
import InfoListItem from './components/InfoListItem.vue'
</script>
