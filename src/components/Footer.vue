<template>
  <footer id="footer">
    <b-container class="footer-wrap pt-5">
      <b-row>
        <b-col class="text-left">
            <strong>Social Media Links</strong><br>
            <a href="https://www.hackerrank.com/samericksn">Hacker Rank</a><br>
            <a href="https://github.com/samerickson">Github</a><br>
            <a href="https://codepen.io/samerickson">Codepen</a><br>
            <a href="https://dev.to/samerickson">Dev.to</a><br>
        </b-col>
        <b-col class="text-center">
          <strong>Contact</strong><br>
          <router-link tag="a" to="/contact">Contact Page</router-link><br>
          <a href="mailto:contact@samerickson.me">Send me an email</a><br>
        </b-col>
        <b-col class="text-right">
          <strong>Resources</strong><br>
          <a href="https://feathericons.com/">Feather Icons</a><br>
          <a href="https://simpleicons.org/">Simple Icons</a><br>
          <a href="https://bootstrap-vue.org/">Bootstrap-Vue</a><br>
          <a href="https://vuejs.org/">Vue.js</a>
        </b-col>
      </b-row>
      <p class="text-center">Copyright 2020 Sam Erickson</p>
    </b-container>
  </footer>
</template>

<style scoped>
  #footer {
    background-color: #e9ecef;
    overflow: hidden;
  }
</style>
