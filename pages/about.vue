<template>
  <div>
    <NavBar />
    <div class="section">
      <div class="container">
        <div class="columns  is-centered">
          <div class="column is-half">
            <h1 class="mb-2">About</h1>
            <p
              v-for="paragraph in about.paragraphs"
              :key="paragraph"
              class="pb-2"
            >
              {{ paragraph }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import NavBar from '~/components/NavBar'
import about from '~/data/about.json'
export default {
  components: {
    NavBar
  },
  data() {
    return {
      about: JSON.parse(JSON.stringify(about))
    }
  }
}
</script>

<style scoped>
h1 {
  font-size: 3rem;

  font-weight: 600;
}
p {
  font-size: 1.2rem;
  font-weight: 300;
  line-height: 1.2;
}
</style>
