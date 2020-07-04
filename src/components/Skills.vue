<template>
  <b-container>
    <h2 class="my-5">Skills</h2>

    <b-row>
      <b-col cols="4">
        <h3>Technology</h3>
      </b-col>
      <b-col col="8">
        <h3>Skill level</h3>
      </b-col>
    </b-row>
    <hr>
    <!-- The below skills should probably be a component of their own -->
        <!-- Linux -->
    <b-row class="my-4">
      <b-col cols="4">
        <a href=""><h4>Linux</h4></a>
      </b-col>
      <b-col cols="8">
        <b-form-rating v-model="linux" readonly></b-form-rating>
      </b-col>
    </b-row>

    <!-- Virtual Machines -->
    <b-row class="my-4">
      <b-col cols="4">
        <a href=""><h4>Virtual Machines</h4></a>
      </b-col>
      <b-col cols="8">
        <b-form-rating v-model="virtualMachines" readonly></b-form-rating>
      </b-col>
    </b-row>

    <!-- C -->
    <b-row class="my-4">
      <b-col cols="4">
        <a href=""><h4>C</h4></a>
      </b-col>
      <b-col cols="8">
        <b-form-rating v-model="c" readonly></b-form-rating>
      </b-col>
    </b-row>

    <!-- Javascript -->
    <b-row class="my-4">
      <b-col cols="4">
        <a href=""><h4>Javascript</h4></a>
      </b-col>
      <b-col cols="8">
        <b-form-rating v-model="javascript" readonly></b-form-rating>
      </b-col>
    </b-row>

    <!-- Python -->
    <b-row class="my-4">
      <b-col cols="4">
        <a href=""><h4>Python</h4></a>
      </b-col>
      <b-col cols="8">
        <b-form-rating v-model="python" readonly></b-form-rating>
      </b-col>
    </b-row>

    <!-- Vue -->
    <b-row class="my-4">
      <b-col cols="4">
        <a href="">
          <h4>Vue</h4>
        </a>
      </b-col>
      <b-col cols="8">
        <b-form-rating v-model="vue" readonly></b-form-rating>
      </b-col>
    </b-row>

  </b-container>

</template>

<script>
export default {
  data() {
    return {
      c: 3,
      javascript: 3,
      python: 3.5,
      linux: 4.5,
      virtualMachines: 5,
      vue: 3,
    };
  },
};
</script>
