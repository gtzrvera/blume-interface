<template>
  <div>
    <p>{{ task.description }}</p>
  </div>
</template>

<script>
export default {
  name: 'TaskDetails',
  props: {
    task: {
      type: Object,
      required: true
    }
  }
}
</script>
