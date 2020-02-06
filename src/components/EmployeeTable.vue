<template>
  <table id="employee-table">
    <thead>
      <tr>
        <th>Employee name</th>
        <th>Employee email</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Lihle Menzeleleli</td>
        <td>lihle@codex.com</td>
      </tr>
      <tr>
        <td>Andre Vermuleun</td>
        <td>andre@codex.com</td>
      </tr>
      <tr>
        <td>Pholisa Fatyela</td>
        <td>pholisa@codex.com</td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
    name: 'employee-table'
};
</script>

<style>
    button {
        background: green;
        border: 1px solid green;
    }
</style>