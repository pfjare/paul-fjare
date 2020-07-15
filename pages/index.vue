<template>
  <div>
    <NavBar />
    <div>
      <p>Icons</p>
      <font-awesome-icon :icon="['fab', 'linkedin']" />
      <font-awesome-icon :icon="['fab', 'github']" />
      <font-awesome-icon :icon="['fab', 'facebook']" />
      <font-awesome-icon :icon="['fas', 'coffee']" />
    </div>
  </div>
</template>

<script>
import NavBar from '~/components/NavBar'
import resume from '~/data/resume.json'
export default {
  components: {
    NavBar
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
