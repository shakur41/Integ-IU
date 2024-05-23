<template>
    <v-card>
      <v-card-title>
        <h1>Student List Page</h1>
        <v-spacer></v-spacer>
        <v-text-field
          v-model="search"
          append-icon="mdi-magnify"
          label="Search"
          single-line
          hide-details
        ></v-text-field>
      </v-card-title>
      <v-data-table :headers="headers" :items="StudentData" :search="search">
        <template slot="item.actions" slot-scope="{}">
          <v-btn color="#B80000"> DELETE</v-btn>
          <v-btn color="#0079FF"> EDIT</v-btn>
          <v-btn color="#008000 "> SAVE</v-btn>
        </template>
      </v-data-table>
    </v-card>
  </template>
  <script>
  export default {
   
    data() {
      return {
        search: "",
        headers: [
          {
            text: "StudentID",
            align: "start",
            sortable: false,
            value: "attributes.student_no",
          },
          { text: "FirtsName", value: "attributes.first_name" },
          { text: "LastName", value: "attributes.last_name" },
          { text: "MiddleName", value: "attributes.middle_name" },
          { text: "Course", value: "attributes.course" },
          { text: "Year", value: "attributes.year" },
          { text: "Section", value: "attributes.section" },
          { text: "", value: "actions" },
        ],
        StudentData: [

          
        ],
      };
    },

    //allfunctions
    methods: {
      getStudentList(){
          this.$axios.get("http://localhost:1337/api/student-lists")
          .then(response => {
            console.log ("Success");
            console.log(response.data.data)
            this.StudentData = response.data.data

          })
          .catch(error =>{
            console.log("Error");
         
          })
      }
    },

    mounted(){
      
      this.getStudentList();
    }

  };
  </script>
  