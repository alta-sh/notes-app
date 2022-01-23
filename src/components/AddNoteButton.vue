<template>
  <div>
    <v-btn @click.stop="dialog = true" v-if="this.$vuetify.breakpoint.smAndDown" depressed fab small elevation="2" color="blue" dark>
      <v-icon dark>mdi-plus</v-icon>
    </v-btn>
    <v-btn @click.stop="dialog = true" v-else small elevation="5" class="py-4" color="blue" dark>
      <v-icon left dark>mdi-plus</v-icon>
      <span>new note</span>
    </v-btn>

    <NewNoteForm @closeModal="dialog = false" :modal="dialog" />
  </div>
  
</template>

<script>
import NewNoteForm from "@/components/NewNoteForm";

export default {
  name: "AddNoteButton",
  components: {NewNoteForm},


  data() {
    return {
      dialog: false
    }
  }
}
</script>

<style scoped>

</style>