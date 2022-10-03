<template>
  <header class="header sticky-top">
    <NavBar/>
  </header>
  <main>
    <section class="main-banner">
      <MainPhoto/>
    </section>
    <section class="about-us" id="about-us">
      <AboutUs/>
    </section>
    <section class="frameworks" id="frameworks">
      <Frameworks :frameworks="frameworks"/>
    </section>
    <section class="meets-questions">
      <MeetsQuestions/>
    </section>
    <section class="applications" id="applications">
      <MyApplications :applications="applications"/>
    </section>
    <section class="contact-us" id="contact-us">
      <ContactUs/>
    </section>
  </main>
  <footer>
    <MyFooter/>
  </footer>
</template>

<script>
import NavBar from "@/components/NavBar";
import MainPhoto from "@/components/MainPhoto";
import AboutUs from "@/components/AboutUs";
import Frameworks from "@/components/frameworks/MyFrameworks";
import MeetsQuestions from "@/components/MeetsQuestions";
import MyApplications from "@/components/applications/MyApplications";
import ContactUs from "@/components/ContactUs";
import MyFooter from "@/components/MyFooter";


export default {
  name: 'App',
  components: {
    MyFooter,
    ContactUs,
    MyApplications,
    MeetsQuestions,
    Frameworks,
    AboutUs,
    MainPhoto,
    NavBar,
  },
  data() {
    return {
      applications: [
        {id: 0, title: 'App1', filename: 'app1.jpg'}, {id: 1, title: 'App2', filename: 'app2.jpg'},
        {id: 2, title: 'App3', filename: 'app3.jpg'}, {id: 3, title: 'App4', filename: 'app4.jpg'},
        {id: 4, title: 'App5', filename: 'app5.jpg'}, {id: 5, title: 'App6', filename: 'app6.jpg'},
        {id: 6, title: 'App7', filename: 'app7.jpg'}, {id: 7, title: 'App8', filename: 'app8.jpg'},
      ],
      frameworks: [
        {
          id: 0,
          title: 'VueJS',
          filename: 'vue.jpg',
          description: `Vue is a JavaScript framework for building user interfaces.
          It builds on top of standard HTML, CSS and JavaScript, and provides a declarative and component-based programming
          model that helps you efficiently develop user interfaces, be it simple or complex.`,
        },
        {
          id: 1,
          title: 'React',
          filename: 'react.jpg',
          description: `React is a free and open-source front-end JavaScript library for building user interfaces based
          on UI components. It is maintained by Meta (formerly Facebook) and a community of individual developers and
          companies. React can be used as a base in the development of single-page, mobile, or server-rendered applications.`,
        },
        {
          id: 2,
          title: 'Angular',
          filename: 'angular.jpg',
          description: `AngularJS is a discontinued free and open-source JavaScript-based web framework for developing
          single-page applications. It was maintained mainly by Google and a community of individuals and corporations.
          It aimed to simplify both the development and the testing of such applications by providing a framework for client-side.`,
        },
      ]
    }
  }
}
</script>

<style lang="scss">

</style>
