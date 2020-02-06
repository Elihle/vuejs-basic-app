<template>
  <div id="app" class="small-container">
    <h1>Employees</h1>

    <employee-table v-bind:employees="employees"/>
  </div>
</template>

<script>
import EmployeeTable from '@/components/EmployeeTable'

export default {
  name: 'app',
  components: {
    EmployeeTable,
  },

  data() {
    return {
      employees: [
        {
          id: 1,
          name: 'Lihle Menzeleleli',
          email: 'lihle@codex.com'
        },
        {
          id: 2,
          name: 'Andre Vermuleun',
          email: 'andre@codex.com',
        },
        {
          id: 3,
          name: 'Pholisa Fatyela',
          email: 'pholisa@codex.com'
        }
      ]
    }
  }
}
</script>

<style>
  button {
    background: green;
    border: 1px solid green;
  }

  .small-container {
    max-width: 680px;
  }
</style>
