<template>
  <v-app>
    <v-app-bar app absolute flat dark>
     <Heading></Heading>
    </v-app-bar>
    <v-main>
      <FilterNotes></FilterNotes>
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
    //
  }),
};
</script>