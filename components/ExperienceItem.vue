<template>
  <div>
    <div class="columns">
      <div class="column is-full">
        <h4 class="">{{ experience.dates }}</h4>
        <h2>{{ experience.company }}</h2>
        <h3>{{ experience.title }}</h3>

        <ul>
          <li v-for="bullet in experience.bullets" :key="bullet" class="">
            {{ bullet }}
          </li>
        </ul>
      </div>
    </div>
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
