<template>
  <div>
    <v-btn @click.stop="dialog = true" v-if="this.$vuetify.breakpoint.smAndDown" depressed fab small elevation="2" color="blue" dark>
      <v-icon dark>mdi-plus</v-icon>
    </v-btn>
    <v-btn @click.stop="dialog = true" v-else small elevation="5" class="py-4" color="blue" dark>
      <v-icon left dark>mdi-plus</v-icon>
      <span>new note</span>
    </v-btn>

    

    <v-dialog
        v-model="dialog"
        persistent
        retain-focus
        transition="fab-transition"
        max-width="650"
    >
      <v-card>
        <v-row justify="space-between" class="ma-1">
          <v-card-title class="text-h5">
            Create a new note:
          </v-card-title>
          <v-btn @click="dialog = false" small class="mt-2 mx-2" icon color="red">
            <v-icon large>mdi-close</v-icon>
          </v-btn>
        </v-row>
        

        <v-card-text>
          form...
        </v-card-text>

        <v-card-actions class="justify-space-between">

          <v-btn
              color="red darken-1"
              text
              @click="dialog = false"
          >
            reset form
          </v-btn>

          <v-btn
              color="blue darken-1"
              text
              @click="dialog = false"
          >
            Create
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
  
</template>

<script>
export default {
  name: "AddNoteButton",
  
  data() {
    return {
      dialog: false
    }
  }
}
</script>

<style scoped>

</style>