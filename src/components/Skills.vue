<template>
  <b-container>
    <h2 class="my-5">Skills</h2>
    <Skill skill="Virtual Machines" rating="5"/>
    <Skill skill="Javascript" rating="4.5"/>
    <Skill skill="Linux" rating="4"/>
    <Skill skill="Python" rating="3.5"/>
    <Skill skill="NodeJS" rating="4"/>
    <Skill skill="VueJS" rating="4"/>
    <Skill skill="C" rating="3.5"/>
  </b-container>

</template>

<script>
import Skill from '@/components/Skill.vue';

export default {
  components: {
    Skill,
  },
};
</script>
