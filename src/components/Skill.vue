<template>
  <b-row class="my-4">
    <b-col md="4" cols="12">
      <a href=""><h4>{{skill}}</h4></a>
    </b-col>
    <b-col md="8" cols="12">
      <b-form-rating v-model="value" readonly></b-form-rating>
    </b-col>
  </b-row>
</template>

<script>
export default {
  props: [
    'skill',
    'rating',
  ],
  data() {
    return {
      value: parseFloat(this.rating),
    };
  },
};
</script>
