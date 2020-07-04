<template>
  <b-navbar id="header" sticky toggleable="lg" type="dark" variant="primary">
    <b-container>
      <b-navbar-brand>Sam Erickson</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item to="/">Home</b-nav-item>
        <b-nav-item to="/projects">Projects</b-nav-item>
        <b-nav-item to="/contact">Contact</b-nav-item>
        <b-nav-item to="/about">About</b-nav-item>
      </b-navbar-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class=".col-md-4 ml-auto">
        <b-navbar-brand href="https://github.com/samerickson">
          <b-tooltip target="github-icon" triggers="hover">Visit my Github Page</b-tooltip>
          <img
            class='header-icon'
            src="@/assets/icons/github.svg"
            alt="Github icon"
            id="github-icon"
          />
        </b-navbar-brand>
        <b-navbar-brand href="https://codepen.io/samerickson">
          <b-tooltip target="codepen-icon" triggers="hover">Visit my Codepen Page</b-tooltip>
          <img
          class="header-icon"
          src="@/assets/icons/codepen.svg"
          alt="Codepen icon"
          id="codepen-icon">
        </b-navbar-brand>
        <b-navbar-brand href="https://dev.to/samerickson">
          <b-tooltip target="blog-icon" triggers="hover">Visit my blog</b-tooltip>
          <img
          class='header-icon'
          src="@/assets/icons/dev-icon.svg"
          alt="Dev.to icon"
          id="blog-icon"
          >
        </b-navbar-brand>
        <b-navbar-brand href="mailto:contact@samerickson.me">
          <b-tooltip target="mail-icon" triggers="hover">Send me an email</b-tooltip>
          <img
            class='header-icon'
            src="@/assets/icons/mail.svg"
            alt="Mail icon"
            id="mail-tooltip"
          >
        </b-navbar-brand>
      </b-navbar-nav>
    </b-collapse>
    </b-container>
  </b-navbar>
</template>

<script>
export default {
  created() {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      const header = document.getElementById('header');
      if (window.pageYOffset > 0) {
        header.classList.remove('header-no-shadow');
        header.classList.add('header-shadow');
        return;
      }
      header.classList.remove('header-shadow');
      header.classList.add('header-no-shadow');
    },
  },
};
</script>

<style lang="css" scoped>
  .header-icon {
    width: 32px;
    filter: invert(100%);
    margin-right: 0.6em;
    transition: filter 0.5s ease-in-out;
  }
  .header-icon:hover {
    filter: invert(80%);
  }
  .header-shadow {
    transition: box-shadow 1s ease-out;
    box-shadow: 0 1px 1px rgba(0,0,0,0.12),
                2px 2px rgba(0,0,0,0.12),
                0 4px 4px rgba(0,0,0,0.12),
                0 8px 8px rgba(0,0,0,0.12),
                0 16px 16px rgba(0,0,0,0.12);
  }
  .header-no-shadow {
    transition: box-shadow 0.7s ease-in;
  }
</style>
