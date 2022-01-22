<template>
  <v-container>
    <div class="row justify-space-between align-center">
      <span id="site-title" class="display-1">Notes App</span>
      
      <v-col
          cols="4"
          sm="6"
          md="5"
          xl="4"
      >
        <v-text-field
            class="mt-6"
            clearable
            placeholder="Search Notes"
        >
        </v-text-field>
      </v-col>
      
      <AddNoteButton></AddNoteButton>
    </div>
  </v-container>

  
</template>

<script>
import AddNoteButton from "@/components/AddNoteButton";
export default {
  name: "Heading",
  components: {AddNoteButton},
  
}
</script>

<style scoped>
</style>