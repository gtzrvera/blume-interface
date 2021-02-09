<template>
  <header>
    <h1>{{ title }}</h1>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      title: 'Blume ToDo List'
    }
  }
}
</script>

<style scoped>
  h1 {
    font-weight: lighter;
    color: #036F73;
    border-bottom: 5px solid #036F73;
    padding: 10px 0px;
  }
</style>
