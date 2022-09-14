<template>
    <ul>
        <PersonData v-for="(item, index) in employees" 
            :key="index" 
            :name="item.name" 
            :age="item.age" 
            :salary="item.salary" 
            :position="item.position" 
            :gender="item.gender"
            :skill="item.skill" 
        />
    </ul>
</template>

<script>
import PersonData from './PersonData.vue';
export default {
    name: "ListData",
    components: {
        PersonData,
    },
    props: [
        "employees"
    ]
}
</script>

<style scoped>
    ul {
        list-style: none;
        margin: 1rem 0;
        padding: 0;
    }
</style>