<template>
    <header>
        <h1>ระบบจัดการข้อมูลพนังงาน</h1>
    </header>
    <FormComponent @save="insertEmplyees" />
    <section class="employees-content" v-if="employees.length > 0">
        <h2>ข้อมูลพนักงาน</h2>
        <ListData :employees="employees" />
    </section>
</template>

<script>
import ListData from './components/ListData.vue';
import FormComponent from './components/FormComponent.vue';

export default {
    name: "App",
    components: {
        ListData,
        FormComponent
    },
    data() {
        return {
            employees: [

            ]
        }
    },
    methods: {
        insertEmplyees(data) {
            this.employees.push(data)
        }
    }
}
</script>

<style>
    * {
        box-sizing: border-box;
    }

    body {
        margin: 0;
    }

    header {
        color: #ffffff;
        box-shadow: 0 2px 8px rgba(0, 0, 0, .50);
        background: #252525;
        padding: .5em;
        margin: 1em;
        border-radius: 15px;
        text-align: center;
    }
    .employees-content {
        box-shadow: 0 2px 8px rgba(0, 0, 0, .50);
        padding: .5em;
        margin: 1em;
        border-radius: 15px;
        text-align: center;
    }
    
    .employees-content h2 {
        font-size: 2rem;
        border-bottom: 1px solid #252525;
        color: purple;
    }
</style>