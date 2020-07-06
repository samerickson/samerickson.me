<template>
  <b-container class="mb-5 mb-md-0">
    <h1 class="mt-5 mb-4">Projects</h1>
    <ProjectHighlights />
  </b-container>
</template>

<script>
import ProjectHighlights from '@/components/ProjectHighlights.vue';

export default {
  components: {
    ProjectHighlights,
  },
};
</script>
