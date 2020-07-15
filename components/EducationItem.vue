<template>
  <div>
    <div class="columns">
      <div class="column is-full">
        <h3 class="">{{ education.graduation_date }}</h3>
        <h2 class="">{{ education.degree }}</h2>
        <h3 class="">{{ education.school }}</h3>

        <ul v-for="bullet in education.bullets" :key="bullet" class="">
          <li class="">
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
