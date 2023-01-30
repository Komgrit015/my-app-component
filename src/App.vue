<template>
    <div>
  
      <FormComponent/>
      <ListData :employees="employees"/>
    </div>
</template>

<script>
import FormComponent from './components/FormComponent.vue'
import ListData from './components/ListData.vue'
export default{

  name :"App",
  components:{
      ListData,
      FormComponent
  },
  data(){
    return{
        employees:[
          {name:"Mark",salary:"35000"},
          {name:"John",salary:"37000"},
          {name:"Duck",salary:"12000"},
          {name:"Ray",salary:"50000"},
          {name:"Juk",salary:"22000"}

        ]
    }
  }
}

</script>
