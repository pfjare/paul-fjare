<template>
  <div>
    <section class="hero is-fullheight main">
      <div class="hero-head">
        <img
          title="Paul Fjare"
          src="~/assets/pfj_main.svg"
          alt="PFj"
          class="logo"
        />
      </div>
      <div class="hero-body">
        <div class="container">
          <div class="columns is-centered">
            <div class="column is-one-third  has-text-centered">
              <div class="menu">
                <nuxt-link to="/about" class="has-text-centered"
                  >About</nuxt-link
                >
                <nuxt-link to="/blog" class="has-text-centered">Blog</nuxt-link>
                <nuxt-link to="/resume" class="has-text-centered"
                  >Resume</nuxt-link
                >
              </div>
            </div>
            <div class="column is-one-third ">
              <figure class="image">
                <img class="profile-image" src="~/assets/me.jpg" />
              </figure>
              <!-- <h1 class="tagline">
                Hi! I’m Paul Fjare. <br />
                Welcome to my site.
              </h1> -->
            </div>
          </div>
        </div>
      </div>
      <div class="hero-foot has-text-centered">
        <div class="container is-centered">
          <div>
            <div class="social-buttons ">
              <a
                class="button social-icon"
                href="https://github.com/pfjare"
                target="blank"
              >
                <span class="icon is-medium fa-lg"
                  ><fa :icon="['fab', 'github']" />
                </span>
              </a>
              <a
                class="button social-icon"
                href="https://gitlab.com/pfjare"
                target="blank"
              >
                <span class="icon is-small fa-lg"
                  ><fa :icon="['fab', 'gitlab']" />
                </span>
              </a>
              <a
                class="button social-icon"
                href="https://linkedin.com/in/paulfjare"
                target="blank"
              >
                <span class="icon is-small fa-lg"
                  ><fa :icon="['fab', 'linkedin']" />
                </span>
              </a>
              <a
                class="button social-icon"
                href="https://instagram.com/pfjare"
                target="blank"
              >
                <span class="icon is-small fa-lg"
                  ><fa :icon="['fab', 'instagram']" />
                </span>
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
// import NavBar from '~/components/NavBar'
import resume from '~/data/resume.json'
export default {
  components: {},
  data() {
    return {
      resume: JSON.parse(JSON.stringify(resume))
    }
  }
}
</script>

<style scoped>
.menu {
  font-size: 4rem;
  margin-bottom: 0.2rem;
  font-weight: 600;
  color: black;
}
.menu a {
  width: 100%;
}
.tagline {
  font-size: 2.5rem;

  font-weight: 500;
  margin-top: 1rem;
  color: black;
}
.profile-image {
  display: block;
  border-radius: 100%;
  max-width: 300px;
  margin: 0 auto;
}
.logo {
  display: block;

  margin: 0 auto;
}
.social-buttons {
  margin-bottom: 1rem;
  font-size: 3rem;
}
.social-icon {
  background-color: transparent;
  height: 50px;
  width: 50px;
  border: 3px solid black;
  color: black;
  margin: 0 0.5rem;
  border-radius: 100%;
}
.social-icon:hover {
  background-color: white;

  color: black;
}
.social-icon:focus {
  box-shadow: none;
}
.main {
  background-color: #7fffc8;
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
