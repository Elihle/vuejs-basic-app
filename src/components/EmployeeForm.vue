<template>
    <div id="employee-form">
        <form v-on:submit="handleSubmit">
            <label>Employee Name</label>
            <input v-model="employee.name" type="text">
            <label>Employee Email</label>
            <input v-model="employee.email" type="text">
            <button>Add Employee</button>
        </form>
    </div>
</template>

<script>
export default {
    name: 'employeee-form',
    data() {
        return {
            employee: {
                name: '',
                email: '',
            },
        }
    },

    methods: {
        handleSubmit() {
            this.$emit('add:employee', this.employee)
                        
        },
    },
}

</script>

<style scoped>
    form {
        margin-bottom: 2rem;
    }
</style>