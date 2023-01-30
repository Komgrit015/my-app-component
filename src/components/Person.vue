<template>
   <div>
        <h1>Name : {{ name }} Salary: {{ salary }}</h1>
    </div>
</template>

<script>
export default {
    name:"Person",
    props: ["name","salary"]
}
</script>

<style scoped>
    h1{
        color: red;
    }

</style>