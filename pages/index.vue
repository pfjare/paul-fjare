<template>
  <div>
    <NavBar />
    <section class="hero is-fullheight main">
      <div class="hero-head"></div>
      <div class="hero-body">
        <div class="container">
          <div class="columns is-centered">
            <div class="column is-half has-text-centered">
              <img class="profile-image" src="~/assets/me.jpg" />

              <h1 class="tagline">
                Hi! I’m Paul Fjare. <br />
                Welcome to my site.
              </h1>
            </div>
          </div>
        </div>
      </div>
      <div class="hero-foot"></div>
    </section>
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
.tagline {
  font-size: 2.5rem;

  font-weight: 500;
  margin-top: 1rem;
}
.profile-image {
  display: block;
  border-radius: 100%;
  height: 300px;
  width: 300px;
  margin: 0 auto;
}
.main {
  background-color: #7fffc8;
  margin-top: -4rem;
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
