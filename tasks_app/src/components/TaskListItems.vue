<template>
  <ul class="taskListItems">
    <li v-for="task in taskList" :key="task.taskDescription">
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
