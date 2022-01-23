<template>
  <v-container>
    <v-toolbar flat>
      <v-row justify="center" justify-sm="end">

        <span class="text--secondary mt-2">Sort by:</span>
        <v-col
            class="ma-0"
            cols="9"
            sm="3"
            md="3"
            lg="2"
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
      defaultSelected: '↓ Most Recent', 
      items: ['↑ Oldest', '↓ Most Recent',]
    }
  }
  
}
</script>

<style scoped>

</style>