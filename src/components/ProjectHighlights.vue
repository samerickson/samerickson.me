<template>
  <div>
    <Project
      demo="craps_demo.gif"
      title="Craps Simulator"
      date="June 2020"
      github="https://github.com/samerickson/craps"
    >
        <p>
          This project was created to determine the average wins and losses that
          will result in a set number of craps games, and what the longest win
          and lose streaks would be.
        </p>
        <p>
          The plan is to be able to specify <code>startingCash</code>
          and completely simulate a game with a predetermined betting
          strategy and print the output to the user.
        </p>
    </Project>
  </div>
</template>

<script>
import Project from '@/components/Project.vue';

export default {
  components: {
    Project,
  },
};
</script>
