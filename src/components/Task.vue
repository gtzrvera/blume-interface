<template>
  <div class="card">
    <div class="card-body">
      {{ task.name }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'Task',
  props: {
    task: {
      type: Object,
      required: true
    }
  }
}
</script>
