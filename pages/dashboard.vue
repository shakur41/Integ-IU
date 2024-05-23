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
       
      ],
    };
  },
};
</script>
