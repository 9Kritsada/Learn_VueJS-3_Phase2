<template>
    <li>
        <img src="https://seeklogo.com/images/G/github-logo-7880D80B8D-seeklogo.com.png" />
        <hr>
        <slot name="card-header"></slot>
        <slot name="card-button"></slot>
        <slot name="card-content"></slot>
    </li>
</template>
<script>
export default {
    name: "CardData",
}
</script>

<style scoped>
    li {
        color: #ffffff;
        margin: 1em 0;
        font-size: 1.23rem;
        background: #0062ff;
        border-radius: 5px;
        padding: 1em;
    }
    img {
        width: 150px;
        height: auto;
    }
</style>