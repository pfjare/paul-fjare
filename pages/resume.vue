<template>
  <div id="resume">
    <NavBar />
    <div class="section pb-0">
      <div class="container">
        <div class="columns is-centered">
          <div class="column is-half ">
            <div class="resume-info has-text-centered">
              <h1 class="resume-title">Paul Fjare</h1>
              <h2 class="resume-subtitle">Software Engineer</h2>
              <p>Laurel, MT, USA</p>
              <p>pfjare@gmail.com</p>
              <p class="employment has-text-weight-semibold">
                Actively seeking employment
              </p>
            </div>
            <p class="px-2 pt-3">
              Software Engineer transitioning from a career as a Mechanical
              Engineer that provided experience in using code to solve
              real-world problems and in analyzing data. Proven ability to
              respond to customer feedback and to work within a team to solve
              complex technical problems and develop products.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="section ">
      <div class="container">
        <div class="columns  is-centered">
          <div class="column is-half">
            <div class="resume-section">
              <div class="px-3 py-3" style="position: relative;">
                <h1 class="">Skills</h1>
                <div v-on:click="sectionCollapse" class="collapse-button">
                  <span class="collapse-icon"
                    ><fa :icon="['fas', 'minus']" />
                  </span>
                  <span class="collapse-icon hidden"
                    ><fa :icon="['fas', 'plus']"
                  /></span>
                </div>
              </div>
              <div class="resume-section-content">
                <div class="divider"></div>
                <div class="skill-list px-3 py-2">
                  <div
                    v-for="skill in resume.skills"
                    :key="skill.id"
                    class="skill-item"
                  >
                    <SkillItem :skill="skill" />
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="section pt-0">
      <div class="container">
        <div class="columns  is-centered">
          <div class="column is-half">
            <div class="resume-section">
              <div class="px-3 py-3" style="position: relative;">
                <h1 class="">Education</h1>
                <div v-on:click="sectionCollapse" class="collapse-button">
                  <span class="collapse-icon"
                    ><fa :icon="['fas', 'minus']" />
                  </span>
                  <span class="collapse-icon hidden"
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
    <div class="section pt-0">
      <div class="container">
        <div class="columns  is-centered">
          <div class="column is-half">
            <div class="resume-section">
              <div class="px-3 py-3" style="position: relative;">
                <h1 class="">Experience</h1>
                <div v-on:click="sectionCollapse" class="collapse-button">
                  <span class="collapse-icon"
                    ><fa :icon="['fas', 'minus']" />
                  </span>
                  <span class="collapse-icon hidden"
                    ><fa :icon="['fas', 'plus']"
                  /></span>
                </div>
              </div>
              <div class="resume-section-content">
                <div class="divider"></div>
                <div
                  v-for="experience in resume.experiences"
                  :key="experience.id"
                  class="education-item"
                >
                  <ExperienceItem :experience="experience" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="section pt-0">
      <div class="container">
        <div class="columns  is-centered">
          <div class="column is-half">
            <div class="resume-section">
              <div class="px-3 py-3" style="position: relative;">
                <h1 class="">Projects</h1>
                <div v-on:click="sectionCollapse" class="collapse-button">
                  <span class="collapse-icon"
                    ><fa :icon="['fas', 'minus']" />
                  </span>
                  <span class="collapse-icon hidden"
                    ><fa :icon="['fas', 'plus']"
                  /></span>
                </div>
              </div>
              <div class="resume-section-content">
                <div class="divider"></div>
                <div
                  v-for="project in resume.projects"
                  :key="project.id"
                  class="education-item"
                >
                  <ProjectItem :project="project" />
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
import ExperienceItem from '~/components/ExperienceItem'
import EducationItem from '~/components/EducationItem'
import ProjectItem from '~/components/ProjectItem'
import SkillItem from '~/components/SkillItem'
import NavBar from '~/components/NavBar'
import resume from '~/data/resume.json'
export default {
  components: {
    NavBar,
    EducationItem,
    ExperienceItem,
    ProjectItem,
    SkillItem
  },
  methods: {
    sectionCollapse(event) {
      event.currentTarget
        .closest('.resume-section')
        .querySelector('.resume-section-content')
        .classList.toggle('collapsed')

      const collapseIcons = event.currentTarget.querySelectorAll(
        '.collapse-icon'
      )

      collapseIcons.forEach(function(icon) {
        icon.classList.toggle('hidden')
      })
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
}

.resume-section {
  border: 2px solid black;
  border-top: 6px solid black;
}
.resume-info {
  display: block;
}
.resume-title {
  font-size: 2rem;
  margin-bottom: 0.2rem;
  font-weight: 400;
}
.resume-subtitle {
  font-size: 1.3rem;
  margin-top: 0.8rem;
  margin-bottom: 1rem;
  font-weight: 600;
}
.collapse-icon {
  transition-property: color;
  transition-duration: 0.5s;
  position: absolute;
  right: 0;
  top: 0;
  display: block;
}

.education-item {
  padding: 0.75rem;
}
.hidden {
  color: transparent;
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
