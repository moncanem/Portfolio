<template>
    <main>
        <HeaderNav/>
        <DescriptionSection/>
        <AboutSection/>
        <ServicesSection/>
        <PortfolioSection/>
        <ContactSection/>
        <FooterComponent/>
    </main>
</template>

<script>
import HeaderNav from './sections/HeaderNav.vue'
import DescriptionSection from './sections/DescriptionSection.vue'
import AboutSection from './sections/AboutSection.vue'
import ServicesSection from './sections/ServicesSection.vue'
import PortfolioSection from './sections/PortfolioSection.vue'
import ContactSection from './sections/ContactSection.vue'
import FooterComponent from './sections/FooterComponent.vue'

export default {
    name: "MainContent",
    components: {
        HeaderNav,
        DescriptionSection,
        AboutSection,
        ServicesSection,
        PortfolioSection,
        ContactSection,
        FooterComponent
    },
    data() {
    return {
      darkMode: false,
    };
  },
}
</script>

<style>
    * {
    margin: 0;
    padding: 0;
    /* font-family: 'Poppins', sans-serif; */
    box-sizing: border-box;
    }

    main {
        width: 100%;
        /* height: 100vh; */
    }

    
</style>