<template>
  <table id="employee-table">
    <thead>
      <tr>
        <th>Employee name</th>
        <th>Employee email</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="employee in employees" v-bind:key="employee.id">
        <td>{{employee.name}}</td>
        <td>{{employee.email}}</td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
    name: 'employee-table',
    props: {
        employees: Array,
    }
};
</script>

<style>
    button {
        background: green;
        border: 1px solid green;
    }
</style>