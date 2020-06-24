<template>
  <div class="header-nav">
    <div class="header-title">
      <h2 class="header-title">PF</h2>
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
#bar {
  height: 200px;
  background-color: blue;
}
#main {
  max-width: 700px;
  margin: 0 auto;
}
.header-title {
  font-family: 'Barlow Condensed', sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
.header-nav {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  border-bottom: 1px solid rgba(0, 0, 0, 0.2);
  transition: box-shadow 200ms ease-in-out;
  background: #fff;
  color: rgba(0, 0, 0, 0.6);
  fill: rgba(0, 0, 0, 0.6);
  box-shadow: 1px 1px transparent;
}
</style>
