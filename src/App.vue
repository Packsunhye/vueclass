<template>
  <div>
  <HeaderLayout fonts="nexon"/>
  <SliderSecrion />
  <ImageSection attr="section nexon" layout="container"/>
  <ImageTextSection attr="section nexon black" layout="container"/>
  <CardSection attr="section nexon scroll" layout="container"/>
  <BannerSection attr="scroll nexon"/>
  <TextSection attr="section nexon scroll" layout="container"/>
  <FooterLayout attr="section nexon scroll gray" layout="container"/>
  </div>
</template>

<script>
import FooterLayout from './components/layout/FooterLayout.vue';
import HeaderLayout from './components/layout/HeaderLayout.vue';
import BannerSection from './components/section/BannerSection.vue';
import CardSection from './components/section/CardSection.vue';
import ImageSection from './components/section/ImageSection.vue';
import ImageTextSection from './components/section/ImageTextSection.vue';
import SliderSecrion from './components/section/SliderSecrion.vue';
import TextSection from './components/section/TextSection.vue';

export default {
  name: 'App',
  components: {
    HeaderLayout,
    FooterLayout,
    ImageSection,
    ImageTextSection,
    CardSection,
    BannerSection,
    TextSection,
    SliderSecrion
}
}
</script>
