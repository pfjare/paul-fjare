<template>
  <div id="index">
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
            <div class="column is-full is-half-widescreen">
              <div class="container">
                <div class="level">
                  <div class="level-item">
                    <ul class="menu ">
                      <li class="nav-list-item">
                        <nuxt-link to="/about" class="">About</nuxt-link>
                      </li>
                      <li class="nav-list-item">
                        <nuxt-link to="/blog" class="">Blog</nuxt-link>
                      </li>
                      <li class="nav-list-item">
                        <nuxt-link to="/resume" class="">Resume</nuxt-link>
                      </li>
                    </ul>
                  </div>
                  <div class=" level-item">
                    <figure class="image ">
                      <img class="profile-image" src="~/assets/me_c.jpg" />
                    </figure>
                  </div>
                </div>
              </div>
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
export default {}
</script>

<style scoped>
#index {
}
.logo {
  display: block;
  max-width: 300px;
  margin: 3rem auto 0 auto;
}
.social-buttons {
  margin-bottom: 2rem;
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
</style>
