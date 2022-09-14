<template>
    <form @submit.prevent="submitForm">
        <div class="form-control">
            <label for="emp-name">Name</label>
            <input type="text" v-model.trim="employees.name">
        </div>
        <div class="form-control">
            <label for="emp-age">Age</label>
            <input type="text" v-model="employees.age">
        </div>
        <div class="form-control">
            <label for="emp-salary">Salay</label>
            <input type="number" v-model="employees.salary">
        </div>
        <div class="form-control">
            <label for="emp-position">ตำแหน่งงาน</label>
            <select v-model="employees.position">
                <option value="Programer">Programer</option>
                <option value="Production">Production</option>
            </select>
        </div>
        <div class="form-control">
            <h2>เพศ</h2>
            <div>
                <input type="radio" value="ชาย" v-model="employees.gender">
                <label for="emp-gender">ชาย</label>
            </div>
            <div>
                <input type="radio" value="หญิง" v-model="employees.gender">
                <label for="emp-gender">หญิง</label>
            </div>
        </div>
        <div class="form-control">
            <h2>ทักษะ ด้านภาษา</h2>
            <div>
                <input type="checkbox" value="อังกฤษ" v-model="employees.skill">
                <label for="emp-skill">อังกฤษ</label>
            </div>
            <div>
                <input type="checkbox" value="จีน" v-model="employees.skill">
                <label for="emp-skill">จีน</label>
            </div>
            <div>
                <input type="checkbox" value="ญี่ปุ่น" v-model="employees.skill">
                <label for="emp-skill">ญี่ปุ่น</label>
            </div>
        </div>
        <div>
            <button>บันทึกข้อมูล</button>
        </div>
    </form>
</template>

<script>
export default {
    name: "FormComponent",
    data() {
        return {
            employees: {
                name: "",
                age: "",
                salary: 0,
                position: "",
                gender: "",
                skill: []
            }
        }
    },
    methods: {
        submitForm() {
            const newEmployees = {
                name: this.employees.name,
                age: this.employees.age,
                salary: this.employees.salary,
                position: this.employees.position,
                gender: this.employees.gender,
                skill: this.employees.skill               
            }
            this.$emit("save", newEmployees)
            this.resetForm()
        },
        resetForm() {
            this.employees.name = "Krit",
            this.employees.age = "",
            this.employees.salary = 0,
            this.employees.position = "",
            this.employees.gender = "",
            this.employees.skill = []
        }
    }
}
</script>

<style scoped>
    form {
        margin: 2rem auto;
        max-width: 40rem;
        box-shadow: 0 2px 10px rgba(0, 0, 0, .5);
        border-radius: 10px;
        background: #ffffff;
        padding: 2rem;
    }
   .form-control {
        margin: .5rem 0;
    }
    label {
        font-weight: bold;
    }
    input,
    select {
        display: block;
        width: 100%;
        font: inherit;
        margin-top: .5rem;
    }
    button {
        font: inherit;
        background: rebeccapurple;
        color: #ffffff;
        cursor: pointer;
        padding: 0.5rem 1rem;
        border-radius: 10px;
    }
    input[type="radio"],
    input[type="checkbox"] {
        display: inline-block;
        width: auto;
        margin-left: .5rem;
    }
    input[type="radio"] + label,
    input[type="checkbox"] + label {
        font-weight: normal;
    }
    h2 {
        font-size: 1rem;
        margin: .5rem 0;
    }
</style>
