<template>
    <div>
        <h1>Student List</h1>
      <ul v-if = "showList">
        <li v-for="(student, index) in students" :key="students.name">
          :class ="{highlight: student.score >= 70}">
          {{ student.name }}  {{ student.score }}
            {{ name }}
        </li>
      </ul>  
      
      <h3>Passing Students: {{ passingStudents }}</h3>
    </div>
</template>

<script>
  export default{
    data(){
      return{
        showList: true,
        students:[
          {name: "Elyn" , score:80},
          {name: "Lyka" , score:75},
          {name: "Thea",  score:90},

        ]
      }
    },
    computed:{
      passingStudents(){
        return this.students.filter(student => student.score >= 70).length;
      }
    }
  };
</script>
