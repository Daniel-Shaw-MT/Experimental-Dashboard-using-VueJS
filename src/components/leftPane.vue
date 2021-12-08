<template>
  <v-col cols="1">
    <v-sheet rounded="lg">
      <v-list color="transparent">
        <v-list-item link color="grey lighten-4">
          <v-list-item-content>
            <v-icon>mdi-account</v-icon>
          </v-list-item-content>
        </v-list-item>
        <v-divider class="my-2"></v-divider>
        <v-list-item class="" v-for="item in items" :key="item" link>
          <v-tooltip left>
            <template v-slot:activator="{ on, attrs }">
              <v-list-item-content v-bind="attrs" v-on="on">
                <v-icon v-text="item.icon"></v-icon>
                <!-- <v-list-item-title class="ml-2">{{ item.title }} </v-list-item-title> -->
              </v-list-item-content>
            </template>
            <span>{{ item.desc }}</span>
          </v-tooltip>
        </v-list-item>

        <v-divider class="my-2"></v-divider>
        <v-list-item link color="grey lighten-4">
          <v-list-item-content>
            <v-icon>mdi-logout</v-icon>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-sheet>
  </v-col>
</template>

<script>
export default {
  beforeMount() {},
  methods: {},
  data: () => ({
      items: [
      {
        icon: "mdi-plus",
        desc: "Add"
      },
      {
        icon: "mdi-calendar",
      },
      {
        icon: "mdi-cash",
      },
      {
        icon: "mdi-pencil",
      },
      {
        icon: "mdi-cog",
      },
    ],

  }),
};
</script>

<style>
</style>