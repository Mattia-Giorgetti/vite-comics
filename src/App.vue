<template>
  <HeaderComponent/>
  <main>
  <ContentSectionComponent />
  <IconsSectionComponent />
  <LinkSectionComponent />
  </main>
  <FooterComponent />
</template>

<script>
import ContentSectionComponent from './components/ContentSectionComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import IconsSectionComponent from './components/IconsSectionComponent.vue';
import LinkSectionComponent from './components/LinkSectionComponent.vue';

  export default {
    components: { FooterComponent, ContentSectionComponent, IconsSectionComponent, LinkSectionComponent, HeaderComponent }
}
</script>

<style lang="scss" scoped>

</style>