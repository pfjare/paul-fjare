<template>
  <div>
    <NavBar />
    <div id="main">
      <b-container fluid="sm">
        <h1>Education</h1>
        <div
          v-for="education in resume.education"
          :key="education.id"
          sm="12"
          class="mt-3 h-100"
        >
          <EducationItem :education="education" />
        </div>
        <h1>Experience</h1>
        <b-row class="mt-3">
          <b-col
            v-for="experience in resume.experiences"
            :key="experience.id"
            sm="12"
            class="mt-3 h-100"
          >
            <ExperienceItem :experience="experience" />
          </b-col>
        </b-row>
      </b-container>
    </div>
  </div>
</template>

<script>
import ExperienceItem from '~/components/ExperienceItem'
import EducationItem from '~/components/EducationItem'
import NavBar from '~/components/NavBar'
import resume from '~/data/resume.json'
export default {
  components: {
    NavBar,
    ExperienceItem,
    EducationItem
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
  font-family: 'Barlow Condensed', sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
#main {
  max-width: 700px;
  margin: 0 auto;
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
