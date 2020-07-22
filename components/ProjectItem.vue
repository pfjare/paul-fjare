<template>
  <div>
    <div class="columns">
      <div class="column is-full">
        <h3 class="">{{ project.dates }}</h3>
        <h2>{{ project.title }}</h2>

        <ul v-for="bullet in project.bullets" :key="bullet" class="">
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
  name: 'ProjectItem',
  props: ['project']
}
</script>

<style scoped></style>
