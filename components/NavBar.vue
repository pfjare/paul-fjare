<template>
  <nav
    class="navbar has-shadow is-fixed-top"
    role="navigation"
    aria-label="main navigation"
  >
    <div class="navbar-brand">
      <nuxt-link class="navbar-item" to="/">
        <img src="~/assets/pfj.png" alt="" srcset="" />
      </nuxt-link>

      <a
        ref="burgerToggle"
        role="button"
        class="navbar-burger burger"
        aria-label="menu"
        aria-expanded="false"
        data-target="navbarBasicExample"
        v-on:click="greet"
      >
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>

    <div id="navbarBasicExample" ref="navMenuToggle" class="navbar-menu">
      <div class="navbar-start">
        <a class="navbar-item has-text-centered">
          About
        </a>

        <nuxt-link to="/resume" class="navbar-item has-text-centered"
          >Resume</nuxt-link
        >
      </div>

      <div class="navbar-end">
        <div class="navbar-item has-text-centered">
          <a
            class="button social-icon"
            href="https://github.com/pfjare"
            target="blank"
          >
            <span class="icon is-small"><fa :icon="['fab', 'github']" /> </span>
          </a>
          <a
            class="button social-icon"
            href="https://gitlab.com/pfjare"
            target="blank"
          >
            <span class="icon is-small"><fa :icon="['fab', 'gitlab']" /> </span>
          </a>
          <a
            class="button social-icon"
            href="https://linkedin.com/in/paulfjare"
            target="blank"
          >
            <span class="icon is-small"
              ><fa :icon="['fab', 'linkedin']" />
            </span>
          </a>
          <a
            class="button social-icon"
            href="https://instagram.com/pfjare"
            target="blank"
          >
            <span class="icon is-small"
              ><fa :icon="['fab', 'instagram']" />
            </span>
          </a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'ExperienceItem',
  props: ['experience'],
  methods: {
    greet(event) {
      this.$refs.burgerToggle.classList.toggle('is-active')
      this.$refs.navMenuToggle.classList.toggle('is-active')
    }
  }
}
</script>

<style scoped>
.social-icon {
  background-color: transparent;
  height: 35px;
  width: 35px;
  border: 2px solid black;
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
.fa-fw {
  text-align: center;
}
#bar {
  height: 200px;
  background-color: blue;
}
.nav-main {
  background-color: #7fffc8;
}
.nav-corner {
  width: 60px;
}
.header-title {
  font-family: 'Barlow Condensed', sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
.header-nav {
  display: flex;
  flex-direction: row;
  align-items: flex-start;

  transition: box-shadow 200ms ease-in-out;
  background: rgb(253, 240, 237);
  background: linear-gradient(
    0deg,
    rgba(253, 240, 237, 1) 5%,
    rgba(237, 250, 253, 1) 100%
  );
  color: rgba(0, 0, 0, 0.6);
  fill: rgba(0, 0, 0, 0.6);
  box-shadow: 1px 2px rgba(0, 0, 0, 0.2);
}
</style>
