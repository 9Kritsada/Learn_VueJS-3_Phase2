<template>
    <ul>
        <PersonData v-for="(item, id) in employees" 
            :key="id" 
            :id="item.id" 
            :name="item.name" 
            :age="item.age" 
            :salary="item.salary" 
            :isVisible="item.isVisible"
        />
    </ul>
</template>

<script>
import PersonData from './PersonData.vue';
export default {
    name: "ListData",
    components: {
        PersonData
    },
    data() {
        return {
            employees: [
                {
                    id: 1,
                    name: "John",
                    age: "23",
                    salary: 45000,
                    isVisible: false
                },
                {
                    id: 2,
                    name: "Kong",
                    age: "29",
                    salary: 50000,
                    isVisible: false
                },
                {
                    id: 3,
                    name: "Fire",
                    age: "21",
                    salary: 35000,
                    isVisible: false
                    
                },
                {
                    id: 4,
                    name: "Gel",
                    age: "25",
                    salary: 45000,
                    isVisible: false
                },
                {
                    id: 5,
                    name: "Poon",
                    age: "19",
                    salary: 20000,
                    isVisible: false
                },
                {
                    id: 6,
                    name: "Jirun",
                    salary: 20000,
                    isVisible: false
                },
            ]
        }
    }
}
</script>

<style scoped>
    ul {
        list-style: none;
        margin: 1rem 0;
        padding: 0;
    }
</style>