<template>
    <v-btn v-if="this.$vuetify.breakpoint.smAndDown" depressed fab small elevation="2" color="blue" dark>
      <v-icon dark>mdi-plus</v-icon>
    </v-btn>
    <v-btn v-else small elevation="5" class="py-4" color="blue" dark>
      <v-icon left dark>mdi-plus</v-icon>
      <span>new note</span>
    </v-btn>
</template>

<script>
export default {
  name: "AddNoteButton"
}
</script>

<style scoped>

</style>