<template>
  <div>
    <h4>{{ education.degree }}</h4>
    <h5>{{ education.school }}</h5>
    <h5 class="text-secondary">{{ education.graduation_date }}</h5>
    <ul
      v-for="bullet in education.bullets"
      :key="bullet"
      class="text-justify mb-1 mt-2 list-unstyled"
    >
      <li class="">
        {{ bullet }}
      </li>
    </ul>
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
