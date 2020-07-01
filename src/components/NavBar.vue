<template>
    <div>
  <b-navbar toggleable="lg" type="dark" variant="info">
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
      <b-navbar-nav class="ml-auto">
        <b-navbar-brand href="https://github.com/samerickson">
          <img class='header-icon' src="../assets/icons/github.svg" alt="Github icon">
        </b-navbar-brand>
        <b-navbar-brand href="https://dev.to/samerickson">
          <img class='header-icon' src="../assets/icons/dev-icon.svg" alt="Dev.to icon">
        </b-navbar-brand>
        <b-navbar-brand href="mailto:contact@samerickson.me">
          <img class='header-icon' src="../assets/icons/mail.svg" alt="Mail icon">
        </b-navbar-brand>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</div>
</template>

<style lang="css" scoped>
  .header-icon {
    width: 32px;
    filter: invert(100%);
    margin-right: 0.6em;
  }
  .header-icon:hover {
    filter: invert(80%);
  }
</style>
