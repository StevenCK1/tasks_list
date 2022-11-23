<template>
  <ul class="taskListItems">
    <li v-for="task in taskList" :id="`task-${task.id}`" :key="task.id">
      <p>Your task: {{ task.taskDescription }}</p>
      <p>Priority Number: {{ task.priorityNumber }}</p>
    </li>
  </ul>
</template>

<script>
export default {
  name: "TaskListItems",
  props: { taskList: Array },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
