<template>
  <div>
    <b-card border-variant="primary" :img-src="experience.image" img-top>
      <b-row>
        <b-col class="">
          <h3>{{ experience.company }}</h3>
          <h5>{{ experience.title }}</h5>
          <h5 class="text-secondary">{{ experience.dates }}</h5>
          <ul
            v-for="bullet in experience.bullets"
            :key="bullet"
            class="text-justify mb-1  mt-2 list-unstyled"
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
}
</style>
