<template>
  <b-container>
    <b-row>
      <b-col> </b-col>
    </b-row>
    <b-row class="mt-3">
      <b-col
        v-for="experience in resume.experiences"
        :key="experience.id"
        lg="6"
        class="mt-3 h-100"
      >
        <ExperienceItem :experience="experience" />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import ExperienceItem from '~/components/ExperienceItem'
import resume from '~/data/resume.json'
export default {
  components: {
    ExperienceItem
  },
  data() {
    return {
      resume: JSON.parse(JSON.stringify(resume))
    }
  }
}
</script>

<style>
.title {
  font-family: 'Lato', sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
#main {
  background-color: blue;
  height: 100px;
}
.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
