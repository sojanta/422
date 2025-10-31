<template>
  <div class="task-item">
    <div class="task-content">
      <h3 class="task-title">{{ task.title }}</h3>
      <p class="task-text">{{ task.text }}</p>
    </div>
    <div class="task-id">
      ID: {{ task.id }}
    </div>
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

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');

.task-item {
  background: #ffffff; 
  border-radius: 8px;
  padding: 15px;
  margin-bottom: 15px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); 

  .task-title {
    color: #333; 
    font-size: 1.2rem;
    font-weight: bold;
    margin-bottom: 8px;
  }

  .task-text {
    color: #666; 
    line-height: 1.5;
    font-size: 0.9em;
  }

  .task-id {
    color: #9bbe8b; 
    font-size: 0.8rem;
    float: right;
  }
}
</style>