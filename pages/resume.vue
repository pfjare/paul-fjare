<template>
  <div id="resume">
    <NavBar />
    <div class="section">
      <div class="container">
        <div class="columns  is-centered">
          <div class="column is-half">
            <div class="resume-section">
              <div class="px-3 py-3" style="position: relative;">
                <h1 class="">Education</h1>
                <div v-on:click="educationCollapse" class="collapse-button">
                  <span class="minus"><fa :icon="['fas', 'minus']" /> </span>
                  <span class="plus collapsed"
                    ><fa :icon="['fas', 'plus']"
                  /></span>
                </div>
              </div>
              <div class="resume-section-content">
                <div class="divider"></div>
                <div
                  v-for="education in resume.education"
                  :key="education.id"
                  class="education-item"
                >
                  <EducationItem :education="education" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import ExperienceItem from '~/components/ExperienceItem'
import EducationItem from '~/components/EducationItem'
import NavBar from '~/components/NavBar'
import resume from '~/data/resume.json'
export default {
  components: {
    NavBar,
    EducationItem
    // ExperienceItem,
  },
  methods: {
    educationCollapse(event) {
      event.currentTarget
        .closest('.resume-section')
        .querySelector('.resume-section-content')
        .classList.toggle('collapsed')

      event.currentTarget.querySelector('.minus').classList.toggle('collapsed')

      event.currentTarget.querySelector('.plus').classList.toggle('collapsed')
    }
  },
  data() {
    return {
      resume: JSON.parse(JSON.stringify(resume))
    }
  }
}
</script>

<style>
.collapse-button {
  cursor: pointer;
  position: absolute;
  right: 1rem;
  top: 1rem;
  transition-property: display;
  transition-duration: 0.5s;
}
.minus {
  position: absolute;
  right: 0;
  top: 0;
  display: block;
}
.plus {
  position: absolute;
  right: 0;
  top: 0;
  display: block;
}
.resume-section {
  border: 2px solid black;
}
.divider {
  border-bottom: 2px solid black;
}
.education-item {
  padding: 0.75rem;
}
.collapsed {
  display: none;
}
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
