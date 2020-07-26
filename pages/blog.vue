<template>
  <div>
    <NavBar />
    <div class="section">
      <div class="container">
        <div class="columns  has-text-centered">
          <div class="column">
            <h1>Coming soon!</h1>
          </div>
        </div>
      </div>
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

<style scoped>
h1 {
  font-size: 3rem;

  font-weight: 600;
}
</style>
