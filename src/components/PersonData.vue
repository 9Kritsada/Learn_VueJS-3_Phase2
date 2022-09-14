<template>
    <CardData>
        <!-- Card Header -->
        <template v-slot:card-header>
            <h3>Name: {{name}}</h3>
        </template>
        
        <!-- Card Content -->
        <template v-slot:card-content>
            <p>อายุ {{age}}</p>
            <p>เงินเดือน {{salary}}</p>
            <p>ตำแหน่ง {{position}}</p>
            <p>ทักษะ {{skill}}</p>
            <p>เพศ {{gender}}</p>
        </template>
    </CardData>
</template>

<script>
import CardData from "./CardData.vue"

export default {
    name: "PersonData",
    components : {
        CardData
    },
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
        position: {
            type: String
        },
        gender: {
            type: String,
        },
        skill: {
            type: Array,
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
    .fade-enter-from {
        opacity: 0;
    }
    .fade-enter-active {
        transition: all .5s ease;
    }
</style>