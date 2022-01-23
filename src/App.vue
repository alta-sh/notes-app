<template>
  <v-app>
    <v-app-bar app absolute flat dark>
     <Heading></Heading>
    </v-app-bar>
    
    <v-main>
      <FilterNotes></FilterNotes>
      <v-layout v-if="notes.length === 0" class="mt-16" justify-center>
        <p class="grey--text text--lighten-1">You don't seem to have any notes... 😔</p>
      </v-layout>
    </v-main>

    
  </v-app>
</template>

<script>
import Heading from "@/components/Heading.vue";
import FilterNotes from "@/components/FilterNotes.vue";

export default {
  name: 'App',
  components: {Heading, FilterNotes},
  data: () => ({
    notes: []
  }),
};
</script>