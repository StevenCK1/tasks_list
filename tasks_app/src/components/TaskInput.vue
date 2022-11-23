<template>
  <div class="taskInput">
    <h2>Create a new task</h2>

    <label for="textInput">Task description:</label>
    <input type="text" id="textInput" />
    <label for="priorityNumber"
      >Set the priority of the task (1 is most urgent, 10 is least
      urgent):</label
    >
    <select id="priorityNumber">
      <option value="1">1</option>
      <option value="2">2</option>
      <option value="3">3</option>
      <option value="4">4</option>
      <option value="5">5</option>
      <option value="6">6</option>
      <option value="7">7</option>
      <option value="8">8</option>
      <option value="9">9</option>
      <option value="10">10</option>
    </select>
    <button type="button">Save</button>
  </div>
</template>

<script>
export default {
  name: "TaskInput",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
