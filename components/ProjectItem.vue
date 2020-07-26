<template>
  <div>
    <div class="columns">
      <div class="column is-full">
        <h4 class="">{{ project.dates }}</h4>
        <h2>{{ project.title }}</h2>
        <p>
          {{ project.description }}
        </p>
        <ul>
          <li v-for="bullet in project.bullets" :key="bullet" class="">
            {{ bullet }}
          </li>
        </ul>

        <ul>
          <li
            v-for="link in project.links"
            :key="link"
            class=""
            href="link.url"
          >
            <a>{{ link.title }}</a>
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

<style scoped>
a {
  color: black;
  text-decoration: underline;
}
a:hover {
  text-decoration: none;
}
</style>
