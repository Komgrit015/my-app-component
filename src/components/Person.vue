<template>
    <li>
        <h1>Name : {{ name }}</h1>
        <button>Infornation</button>&nbsp;
        <button>Delete</button>
        <div v-show="isVisible">
            <p> Salary: {{ salary }} ฿ , Department : {{ department }}</p>
        </div>    
    </li>
</template>

<script>
export default {
    name:"Person",
    props: {
        id:{
            type:Number
        },
        name: {
            type: String,
            required: true,
        },
        salary: {
            type: Number,
            default: 15000
        },
        department: {
            type: String,
            required: true
        },
        isVisible: {
            type: Boolean
        }
    }
}
</script>

<style scoped>
    li{
        margin: 1rem 0;
        font-size: 1.25rem;
        font-weight: blod;
        background: #8ddba4;
        padding: 0.5rem;
        color: #1f1f1f;
        border-radius: 25px;
    }

    button{
        font: inherit;
        cursor: pointer;
        border: 1px solid #ff0077;
        background: #ff0077;
        color: #fff;
        padding: 0.05rem 1rem ;
        box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.26);
    }

</style>