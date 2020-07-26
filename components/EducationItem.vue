<template>
  <div>
    <div class="columns">
      <div class="column is-full">
        <h4 class="">{{ education.graduation_date }}</h4>
        <h2 class="">{{ education.degree }}</h2>
        <h3 class="">{{ education.school }}</h3>

        <ul>
          <li v-for="bullet in education.bullets" :key="bullet" class="">
            {{ bullet }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'EducationItem',
  props: ['education']
}
</script>

<style scoped>
ul {
}
</style>
