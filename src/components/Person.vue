<template>
    <Card>
        <template v-slot:card-header>
             <h1>Name : {{ name }}</h1>
        </template>
        <template v-slot:card-button>
            <button @click="showDescription(id)">Infornation</button>&nbsp;
            <button @click="deleteemployee(id)">Delete</button>
        </template>
        <template v-slot:card-content>
            <transition name="fade">
                <div v-show="isVisible">
                    <p> Salary: {{ salary }} ฿ , Department : {{ department }}</p>
                </div>   
            </transition>
        </template>
   
    </Card>
</template>

<script>
import Card from "./Card.vue";
export default {
    name:"Person",
    components: {
        Card,
    },
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
    },
    methods:{
        showDescription(id){
            this.$emit("show",id);
        },
        deleteemployee(id){
            this.$emit("delete",id);
        }
    }
}
</script>

<style scoped>

    button{
        font: inherit;
        cursor: pointer;
        border: 1px solid #ff0077;
        background: #ff0077;
        color: #fff;
        padding: 0.05rem 1rem ;
        box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.26);
    }
    .fade-enter-from{
        opacity: 0;
    }
    .fade-enter-active{
        transition: all 0.5s linear;
    }

</style>