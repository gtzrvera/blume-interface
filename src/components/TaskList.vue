<template>
  <div>
    <Task v-for="task in tasks"
      v-bind:key="task.id"
      v-bind:task="task"
    ></Task>
  </div>
</template>

<script>
import Task from './Task.vue';

export default {
  name: 'TaskList',
  components: {
    Task
  },
  data () {
    return {
      tasks: [
        { id: 1, name: 'Buy milk' },
        { id: 2, name: 'Taking the dog for a walk' },
        { id: 3, name: 'Call mom' }
      ]
    }
  }
}
</script>
