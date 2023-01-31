<template>
  <ul>
    <!-- <Person
      v-for="item in employees"
      :id="item.id"
      :key="item.id"
      :name="item.name"
      :salary="item.salary"
      :department="item.department"
      :isVisible="item.isVisible"
      @show="toggleVisible"
      @delete="removeemployee"
    /> -->
    <Person
      v-for="(item,index) in employees"
      :key="index"
      :name="item.name"
      :salary="item.salary"
      :department="item.department"
      :gender="item.gender"
      :skill="item.skill"
    />
  </ul>
</template>

<script>
import Person from "./Person.vue";
export default {
  name: "ListData",
  components: {
    Person,
  },
  props:["employees"]
//   data() {
//     return {
//       employees: [
//         {
//           id: 1,
//           name: "Mark",
//           salary: 35000,
//           department: "Programmer",
//           isVisible: false,
//         },
//         {
//           id: 2,
//           name: "John",
//           salary: 37000,
//           department: "UX/UI",
//           isVisible: false,
//         },
//         {
//           id: 3,
//           name: "Duck",
//           salary: 12000,
//           department: "Tester",
//           isVisible: false,
//         },
//         {
//           id: 4,
//           name: "Ray",
//           salary: 50000,
//           department: "BA",
//           isVisible: false,
//         },
//         {
//           id: 5,
//           name: "Juk",
//           salary: 22000,
//           department: "PM",
//           isVisible: false,
//         },
//       ],
//     };
//   },
//   methods: {
//     toggleVisible(id) {
//         this.employees = this.employees.map((item) =>{
//             if(item.id === id){
//                 return{...item,isVisible:!item.isVisible}
//             }
//             return item
//         })
//     },
//     removeemployee(id){
//         this.employees = this.employees.filter(item => {
//             return item.id !== id
//         })
//     }
//   },
};
</script>

<style scoped>
ul {
  list-style: none;
  margin: 1rem 0;
  padding: 0;
}
</style>