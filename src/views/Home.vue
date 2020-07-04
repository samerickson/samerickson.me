<template>
  <section>
    <b-jumbotron>
      <b-container>
        <b-row align-v="center">
          <b-col>
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
          <b-col>
            <b-img src="https://openclipart.org/image/2400px/svg_to_png/194077/Placeholder.png" fluid></b-img>
          </b-col>
        </b-row>
      </b-container>
    </b-jumbotron>
    <div class="text-center my-5">
      <b-icon animation="cylon-vertical" icon="chevron-double-down" font-scale="3.2"></b-icon>
    </div>
    <b-row class="my-5">
        <Skills />
    </b-row>
    <b-row class="my-5">
      <Projects/>
    </b-row>
  </section>
</template>

<script>
import Skills from '@/components/Skills.vue';
import Projects from '@/views/Projects.vue';

export default {
  components: {
    Skills,
    Projects,
  },
};
</script>
