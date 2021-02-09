<template>
  <div class="container" id="app">
    <Header></Header>

    <TaskList></TaskList>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import TaskList from './components/TaskList.vue';

export default {
  name: 'App',
  components: {
    Header,
    TaskList
  }
}
</script>
