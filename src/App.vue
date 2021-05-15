<template>
  <div class="w-full h-full md:container md:mx-auto">
    <div id="mobile-header" class="md:hidden">
      <img
        id="mobile-header_image"
        src="/src/assets/img/haus.png"
        class="object-cover h-auto max-w-full md:hidden"
        :width="computedWidth"
        :height="computedHeight"
      />
    </div>
    <hero />
    <div id="image-grid" class="hidden md:block md:m-10">
      <image-grid />
    </div>
    <!-- TODO loop over content-sections -->
    <div id="content">
      <content-section title="Ferienwohnung, Gastgeber ist Micky Maus">
        <template #avatar>
          <img
            src="https://a0.muscache.com/im/pictures/user/4537fb3d-813d-4d9f-a11d-135359870033.jpg?im_w=240"
            alt=""
            class="w-14 h-14 rounded-full"
          />
        </template>
        <template #content>
          <p class="text-xl mt-2 font-normal text-gray-700">
            5 Gäste · 2 Schlafzimmer · 2 Betten · 1 Badezimmer
          </p>
        </template>
      </content-section>

      <content-section title="Allgemeine Infos">
        <template #content>
          <info-list :items="features" :view="true" />
        </template>
      </content-section>

      <content-section>
        <template #content>
          <p class="text-lg font-normal text-gray-700">
            Lorem Ipsum is simply dummy text of the printing and typesetting
            industry. Lorem Ipsum has been the industry's standard dummy text
            ever since the 1500s, when an unknown printer took a galley of type
            and scrambled it to make a type specimen book. It has survived not
            only five centuries, but also the leap into electronic typesetting,
            remaining essentially unchanged.
          </p>
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
          <info-list :items="features" :view="false" />
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

<script>
import Hero from './components/Hero.vue'
import InfoCard from './components/InfoList/InfoCard.vue'
import ContentSection from './components/ContentSection.vue'
import InfoList from './components/InfoList/InfoList.vue'
import Features from './assets/features.json'
import ImageGrid from './components/ImageGrid.vue'

export default {
  components: {
    Hero,
    InfoCard,
    ContentSection,
    InfoList,
    Features,
    ImageGrid,
  },
  data() {
    return {
      features: Features,
    }
  },
  computed: {
    computedWidth() {
      return `${window.innerWidth}`
    },
    computedHeight() {
      const width = window.innerWidth
      return (width / 16) * 9
    },
  },
}
</script>
