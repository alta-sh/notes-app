<template>

    <v-dialog
        v-model="dialog"
        persistent
        retain-focus
        transition="fab-transition"
        max-width="650"
    >
      <v-card>
        <v-card-text class="ma-0 pl-2 pr-1 pr-sm-1 pt-1">
          <v-form
          ref="form"
          v-model="valid"
          lazy-validation
          >
            <v-row class="ma-0">
              <v-col cols="6">
                <v-text-field
                    v-model="noteTitle"
                    required
                    placeholder="Note Title"
                    clearable
                    autofocus
                    solo
                    class="mt-3"
                    dense
                />
              </v-col>
              
              <v-col cols="5">
                <p class="text-sm-center font-weight-bold blue-grey--text text--lighten-3">{{dateTime}}</p>
              </v-col>
              
              <v-col cols="1" class="pt-1 pr-1">
                <v-btn @click="closeModal()" class="float-right" small icon color="red">
                <v-icon large>mdi-close</v-icon>
                </v-btn>
              </v-col>
            </v-row>
            
            <v-textarea
                v-model="noteContent"
                placeholder="Note Content"
                dense
                class="px-8"
            />
          </v-form>
        </v-card-text>

        <v-card-actions class="justify-space-between">
          <v-btn
              color="red darken-1"
              text
              @click="resetForm()"
          >
            reset
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
      valid: true,
      noteTitle: "",
      noteContent: "",
      dateTime: {},
      timer: {},
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
    },
  },
  
  created() {
    this.dateTime = new Date();
    this.timer = setInterval(() => {
      var date = new Date();
      this.dateTime = date.toUTCString().slice(0,-3) ;
    }, 1000);
  },

  methods: {
    
    closeModal() {
      this.$emit("closeModal");
      this.resetForm();
    },
      
    resetForm() {
      this.noteTitle = "";
      this.noteContent = "";
    },
    
    submitForm() {
      console.log("submitting form")
    } 
  }
}
</script>

<style scoped>
</style>