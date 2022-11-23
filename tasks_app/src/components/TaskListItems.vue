<template>
  <div>
    <h2>View your tasks</h2>
    <ul class="taskListItems">
      <li
        v-for="(task, index) in taskList"
        :id="`task-${task.id}`"
        :key="task.id"
      >
        <p>Your task: {{ task.taskDescription }}</p>
        <p>Priority Number: {{ task.priorityNumber }}</p>
        <button @click="$emit('remove', index)">Remove</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "TaskListItems",
  props: { taskList: Array },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
