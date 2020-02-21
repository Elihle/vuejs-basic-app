<template>
  <div id="app" class="small-container">
    <h1>Employees</h1>
  
    <employee-form @add:employee="addEmployee"/>
    <employee-table v-bind:employees="employees"/>
  </div>
</template>

<script>
import EmployeeTable from '@/components/EmployeeTable'
import EmployeeForm from '@/components/EmployeeForm'

export default {
  name: 'app',
  components: {
    EmployeeTable,
    EmployeeForm,
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
          name: 'Andre Vermuelen',
          email: 'andre@codex.com',
        },
        {
          id: 3,
          name: 'Pholisa Fatyela',
          email: 'pholisa@codex.com'
        }
      ]
    }
  },

  methods: {
    addEmployee(employee) {
      this.employees = [...this.employees, employee]

      const lastId = this.employees.length > 0 ? this.employees[this.employees.length - 1].id : 0;
      const id = lastId + 1;
      const newEmployee = {...employee, id};
      this.employees = [...this.employees, newEmployee];
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
