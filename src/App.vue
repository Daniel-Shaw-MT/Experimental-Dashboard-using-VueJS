<template>
  <v-app id="inspire">
    <v-app-bar app flat class="white">
      <v-container class="py-0 fill-height">
        <v-btn v-for="link in links" :key="link" text>
          <v-icon v-text="link"></v-icon>
        </v-btn>

        <v-spacer></v-spacer>
        <!-- 
        <v-responsive max-width="260">
          <v-text-field
            dense
            flat
            hide-details
            rounded
            solo-inverted
          ></v-text-field>
        </v-responsive> -->
        <v-btn v-for="link in linksRight" :key="link" text>
          <v-icon v-text="link"></v-icon>
        </v-btn>

        <!-- <v-spacer></v-spacer> -->
      </v-container>
    </v-app-bar>

    <v-main class="grey lighten-4">
      <v-container>
        <v-row>
          <leftPane></leftPane>
          <lessons></lessons>
          <rightPane></rightPane>
          
          
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import lessons from './components/lessons.vue'
import leftPane from './components/leftPane.vue'
import rightPane from './components/rightPane.vue'
export default {
  components: {
    lessons,
    leftPane,
    rightPane,
  },
  methods: {
    exampleFunc: function () {
      
    },
  },
  beforeMount() {},

  data: () => ({
    // App bar links
    links: ["mdi-home-variant", "mdi-gesture", "mdi-send"],
    linksRight: ["mdi-plus", "mdi-pencil"],
    
  }),
};
</script>