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
        {
          id: 1,
          name: 'Buy milk',
          description: 'Buy milk to make a delicious cake on the weekend'
        },
        {
          id: 2,
          name: 'Taking the dog for a walk',
          description: 'Do not forget to bring the ball to play with Chicles'
        },
        {
          id: 3,
          name: 'Call mom',
          description: 'Congratulate her on her birthday and tell her that on Friday afternoon we will go to dinner '
        }
      ]
    }
  }
}
</script>
