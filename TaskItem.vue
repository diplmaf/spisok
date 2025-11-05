<template>
  <div class="task-item">
    <h3 class="task-title">{{ task.title }}</h3>
    <p class="task-text">{{ task.text }}</p>
  </div>
</template>

<script>
export default {
  name: 'TaskItem',
  props: {
    task: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.task-item {
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  padding: 15px;
  background-color: #f9f9f9;
  margin: 10px 0;
}
</style>