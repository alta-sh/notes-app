<template>
  <v-container>
    <v-toolbar flat>
      <v-row justify="center" justify-sm="end">

        <span class="text--secondary mt-2">Filter by:</span>
        <v-col
            class="ma-0"
            cols="9"
            sm="3"
            md="2"
            xl="1"
        >
          <v-select
          ></v-select>
        </v-col>

      </v-row>
    </v-toolbar>
  </v-container>
</template>

<script>
export default {
  name: "FilterNotes"
}
</script>

<style scoped>

</style>