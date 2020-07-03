<template>
  <section>
    <b-jumbotron>
      <b-container>
        <h1 class="display-3">Sam Erickson</h1>
        <p class="lead">Welcome to my webpage</p>
        <p>I am a computer science student at Vancouver Island University.</p>
        <b-button to="/about" class="mr-2" variant="primary" href="#">Learn More</b-button>
        <b-button to="/projects" variant="success" href="#">See Projects</b-button>
        </b-container>
    </b-jumbotron>
    <Skills />
    <CssArt />
  </section>
</template>

<script>

export default {
  components: {
  },
};
</script>
