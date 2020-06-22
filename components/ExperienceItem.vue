<template>
  <div>
    <b-card border-variant="primary" :img-src="experience.image" img-top>
      <b-row>
        <b-col class="text-right">
          <h3>{{ experience.company }}</h3>
          <h5>{{ experience.title }}</h5>
          <small>{{ experience.dates }}</small>
          <ul
            v-for="bullet in experience.bullets"
            :key="bullet"
            class="text-justify mb-1 "
          >
            <li class="">
              {{ bullet }}
            </li>
          </ul>
        </b-col>
      </b-row>
    </b-card>
  </div>
</template>

<script>
export default {
  name: 'ExperienceItem',
  props: ['experience']
}
</script>

<style scoped>
ul {
  list-style-type: square;
  margin-left: -1em;
}
</style>
