<template>
  <section>
    <b-jumbotron>
      <b-container>
        <b-row align-v="center">
          <b-col cols="12" md="8" lg="6">
            <h1 class="display-3">Sam Erickson</h1>
            <p class="lead">Welcome to my webpage</p>
            <p>
              I am a computer science student at Vancouver Island University
              who loves making virtual machines and playing around with operating systems.
              I currently teach grades 5 and 6 kids computer science.
            </p>
            <b-button to="/about" class="mr-2" variant="primary" href="#">Learn More</b-button>
            <b-button to="/projects" variant="success" href="#">See Projects</b-button>
          </b-col>
          <!-- <b-col class="d-none d-md-block">
            <b-img src="https://images.unsplash.com/photo-1594008037842-11fe03ea82af?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80" fluid></b-img>
          </b-col> -->
        </b-row>
      </b-container>
    </b-jumbotron>
    <div class="text-center md-my-5">
      <b-icon animation="cylon-vertical" icon="chevron-double-down" font-scale="3.2"></b-icon>
    </div>
    <div class="container">
      <b-row class="md-my-5">
        <Skills />
    </b-row>
    <h2 class="mt-5 mb-4">Projects</h2>
    <ProjectHighlights />
    <h2 class="mt-5 mb-4">Css Artwork</h2>
    <CssArt />
    </div>
  </section>
</template>

<script>
import Skills from '@/components/Skills.vue';
import ProjectHighlights from '@/components/ProjectHighlights.vue';
import CssArt from '@/components/CssArt.vue';

export default {
  components: {
    Skills,
    ProjectHighlights,
    CssArt,
  },
};
</script>
