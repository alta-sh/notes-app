<template>
  <v-container>
    <v-toolbar flat>
      <v-row justify="center" justify-sm="end">

        <span class="text--secondary mt-2">Filter date:</span>
        <v-col
            class="ma-0"
            cols="9"
            sm="3"
            md="2"
            xl="1"
        >
          <v-select
              :items=items
              v-model="defaultSelected"
          ></v-select>
        </v-col>

      </v-row>
    </v-toolbar>
  </v-container>
</template>

<script>
export default {
  name: "FilterNotes",
  
  data() {
    return {
      defaultSelected: '↓ Descending', 
      items: ['↑ Ascending', '↓ Descending',]
    }
  }
  
}
</script>

<style scoped>

</style>