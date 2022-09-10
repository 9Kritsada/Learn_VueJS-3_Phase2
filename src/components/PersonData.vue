<template>
    <li>
        <h3>Name: {{name}}</h3>
        <button>Details</button>
        <button>Delete</button>
        <div v-show="isVisible">
            <p>age: {{age}} Years</p>
            <p>Salary: {{salary}} Baht</p>
        </div>
    </li>
</template>

<script>
export default {
    name: "PersonData",
    props: {
        id: {
            type: Number,
            required: true
        },
        name: {
            type: String,
            required: true
        },
        age: {
            type: String,
            default: "ไม่ระบุอายุ"
        },
        salary: {
            type: Number,
            required: true   
        },
        isVisible: {
            type: Boolean,
            required: true
        }
    }
}
</script>

<style scoped>
    button {
        color: #ffffff;
        font-size: .85em;
        cursor: pointer;
        margin: 0 .5em;
        border: 1px solid #ff0077;
        background: #ff0077;
        border-radius: 10px;
    }
    li {
        margin: 1em 0;
        font-size: 1.23rem;
        background: #8ddba4;
        border-radius: 5px;
        padding: 1em;
    }
</style>