<template>
    <div>
        <h3>{{message}}</h3>
    </div>
</template>

<script>
export default {
    name: "FormComponent",
    data() {
        return {
            message: "แบบฟอร์มบันทึกข้อมูลพนักงาน"
        }
    }
}
</script>

<style scoped>
    h3 {
        color : green;
    }
</style>
