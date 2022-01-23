<template>

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
          <v-btn @click="closeModal()" small class="mt-2 mx-2" icon color="red">
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
              @click="resetForm()"
          >
            reset form
          </v-btn>

          <v-btn
              color="blue darken-1"
              text
              @click="submitForm()"
          >
            Create
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  
</template>

<script>
export default {
  name: "NewNoteForm",
  
  data() {
    return {
    }
  },
  
  props: {
      modal: Boolean,
  },
  
  computed: {
    dialog: {
      get(){
        return this.modal;
      },
    }
  },
  
  methods: {
    closeModal() {
      this.$emit("closeModal")
    },
      
    resetForm() {
      console.log("resetting form")
    },
    
    submitForm() {
      console.log("submitting form")
    }  
  }
}
</script>

<style scoped>

</style>