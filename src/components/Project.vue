<template>
  <b-row>
    <b-col lg="7" md="12">
      <img :src="require('@/assets/projects/demos/' + demo + '')" width="100%" />
    </b-col>
    <b-col lg="5" md="12">
      <h3 class="mt-4 mt-lg-0 mt-md-5 mt-sm-5">{{title}}</h3>
      <small class="secondary">Date: {{date}}</small>
      <slot></slot>
      <b-button :href="github">View on Github</b-button>
    </b-col>
  </b-row>
</template>\

<script>
export default {
  props: [
    'demo',
    'title',
    'date',
    'github',
  ],
};
</script>
