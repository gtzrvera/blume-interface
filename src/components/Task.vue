<template>
  <div v-on:click="toggleDetails" class="card">
    <div class="card-body">
      <div class="d-inline-block custom-control custom-checkbox">
        <input
          v-model="isCompleted"
          v-bind:name="inputName"
          v-bind:id="inputName"
          type="checkbox"
          class="custom-control-input">
        <label class="custom-control-label" v-bind:for="inputName"></label>
      </div>
      <h5
        v-bind:class="{ completed: isCompleted }"
        class="d-inline-block card-title">{{ task.name }}</h5>
      
      <TaskDetails
        v-if="showDetails"
        :task="task"
        ></TaskDetails>
    </div>
  </div>
</template>

<script>
import TaskDetails from './TaskDetails.vue';

export default {
  name: 'Task',
  components: {
    TaskDetails
  },
  data () {
    return {
      isCompleted: false,
      showDetails: false
    }
  },
  props: {
    task: {
      type: Object,
      required: true
    }
  },
  computed: {
    inputName () {
      return `completed_${this.task.id}`;
    }
  },
  methods: {
    toggleDetails () {
      this.showDetails = !this.showDetails;
    }
  }
}
</script>

<style scoped>
  h5.completed {
    text-decoration-line: line-through;
  }

  .card {
    margin: 5px 0px;
  }
</style>
