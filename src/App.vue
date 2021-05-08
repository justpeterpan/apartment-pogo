<template>
  <div class="w-full h-full md:container md:mx-auto">
    <div id="mobile-header" class="bg-gradient-to-t from-white md:hidden">
      <img
        src="/src/assets/img/haus.png"
        class="md:hidden"
      />
    </div>
    <hero />
    <div id="image-grid" class="hidden md:block md:m-10">
      <image-grid />
    </div>
    <!-- TODO loop over content-sections -->
    <div id="content">
      <content-section title="Ferienwohnung">
        <template #content>
          🏗️ headline mit namen <br />
          🏗️ #gast, #schlafzimmer, #betten, #zimmer
        </template>
      </content-section>

      <content-section title="Allgemeine Infos">
        <template #content>
          🏗️ infoliste mit icon/headline/beschreibung
        </template>
      </content-section>

      <content-section title="Infotext">
        <template #content>
          🏗️ Kurzer Text mit Infos zur Lage, Anbindung etc.
        </template>
      </content-section>

      <content-section title="Schlafgelegenheiten">
        <template #content>
          <info-card icon="Icon" title="Schlafzimmer 1" details="2 Betten" />
          <br />
          🏗️ Infos erweitern
        </template>
      </content-section>

      <content-section title="Ausstattung">
        <template #content>
          <info-list :items="Features" />
          <br />
          🏗️ Infos erweitern
        </template>
      </content-section>

      <content-section title="Lage">
        <template #content>
          🏗️ Maps einbinden <br />
          🏗️ Beschreibung zur Lage
        </template>
      </content-section>

      <content-section title="Gastgeber">
        <template #content> 🏗️ Infos zum Gastgeber </template>
      </content-section>

      <content-section title="Was man wissen sollte">
        <template #content> 🏗️ Infos erweitern </template>
      </content-section>
    </div>
  </div>
</template>

<script setup>
import Hero from './components/Hero.vue'
import InfoCard from './components/InfoList/InfoCard.vue'
import ContentSection from './components/ContentSection.vue'
import InfoList from './components/InfoList/InfoList.vue'
import Features from './assets/features.json'
import ImageGrid from './components/ImageGrid.vue'
</script>
