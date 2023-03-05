<template>
    <h1>{{ label }}</h1>
</template>

<script>
export default {
    name: 'SectionLabel',
    props: {
        label: {
            type: String,
            required: true
        }
    }
}
</script>

<style scoped>
h1 {
    margin: 5px;
    border-bottom: 2px;
    border-bottom-width: auto;
    border-bottom-style: solid;
    border-bottom-color: #008cf2;
    width: auto;
    text-align: center;
    font-size: 40px;
}

h1:after {
    font-size: 40px;
    content: "";
    background: black;
    position: relative;
    bottom: 0;
    left: 0;
    height: 50%;
    width: 2px;

}
</style>