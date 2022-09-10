<template>
    <div>
        <h3>{{message}}</h3>
        <PersonData/>
        <PersonData/>
    </div>
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
            message: "แสดงรายชื่อพนักงานทุกคน"
        };
    }
}
</script>

<style>

</style>