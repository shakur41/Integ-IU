<template>
  <v-card>
    <v-card-title>
      <h1>DashBoard</h1>
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
      <template slot="item.actions" slot-scope="{  }">
        <v-btn color="#B80000"> DELETE</v-btn>
        <v-btn color="#0079FF"> EDIT</v-btn>
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
          text: "ID",
          align: "start",
          sortable: false,
          value: "StudentID",
        },
        { text: "FirtsName", value: "Firts_Name" },
        { text: "LastName", value: "Last_Name" },
        { text: "MiddleName", value: "Middle_Name" },
        { text: "Course", value: "Course" },
        { text: "Year", value: "Year" },
        { text: "", value: "actions" },
      ],
      StudentData: [
        {
          Firts_Name: "ROLLY",
          StudentID: "21-00509",
          Last_Name: "Arellano",
          Middle_Name: "Alconga",
          Course: "BSIT",
          Year: "3rd",
        },
        {
          Firts_Name: "ADRIAN",
          StudentID: "21-00549",
          Last_Name: "DASH",
          Middle_Name: "ASlAG",
          Course: "BSIT",
          Year: "3rd",
        },
        {
          Firts_Name: "MANOK",
          StudentID: "21-00519",
          Last_Name: "BONJOUR",
          Middle_Name: "AlSAG",
          Course: "BSIT",
          Year: "3rd",
        },
        {
          Firts_Name: "MAK",
          StudentID: "21-00529",
          Last_Name: "BONJOUR",
          Middle_Name: "AlSAG",
          Course: "BSIT",
          Year: "3rd",
        },
        {
          Firts_Name: "MAK1",
          StudentID: "21-00589",
          Last_Name: "BONJOUR",
          Middle_Name: "AlsAG",
          Course: "BSIT",
          Year: "3rd",
        },
        {
          Firts_Name: "MAK2",
          StudentID: "21-00519",
          Last_Name: "BONJOUR",
          Middle_Name: "AlSAZG",
          Course: "BSIT",
          Year: "3rd",
        },
        {
          Firts_Name: "MAK3",
          StudentID: "21-00589",
          Last_Name: "BONJOUR",
          Middle_Name: "AlSAQG",
          Course: "BSIT",
          Year: "3rd",
        },
        {
          Firts_Name: "MAK5",
          StudentID: "21-00509",
          Last_Name: "BOBJOUR",
          Middle_Name: "AlSGAG",
          Course: "BSIT",
          Year: "3rd",
        },
        {
          Firts_Name: "MAK",
          StudentID: "21-00529",
          Last_Name: "BONJOUR",
          Middle_Name: "AlSAG",
          Course: "BSIT",
          Year: "3rd",
        },
        {
          Firts_Name: "MAK",
          StudentID: "21-00529",
          Last_Name: "BONJOUR",
          Middle_Name: "AlSYUG",
          Course: "BSIT",
          Year: "3rd",
        },
        {
          Firts_Name: "MAK",
          StudentID: "21-00529",
          Last_Name: "BONJOUR",
          Middle_Name: "AlSEG",
          Course: "BSIT",
          Year: "3rd",
        },
        {
          Firts_Name: "MAK",
          StudentID: "21-00529",
          Last_Name: "BONJOUR",
          Middle_Name: "AlSIG",
          Course: "BSIT",
          Year: "3rd",
        },
        {
          Firts_Name: "MAK",
          StudentID: "21-00529",
          Last_Name: "BONJOUR",
          Middle_Name: "AlSOG",
          Course: "BSIT",
          Year: "3rd",
        },
      ],
    };
  },
};
</script>
