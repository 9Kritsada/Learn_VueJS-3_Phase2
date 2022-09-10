<template>
    <div>
        <h1>App Component</h1>
        <FormComponent/>
        <ListData/>
    </div>
</template>

<script>
import ListData from './components/ListData.vue';
import FormComponent from './components/FormComponent.vue';

export default {
    name: "App",
    components: {
        ListData,
        FormComponent
    }
}
</script>

<style>

</style>