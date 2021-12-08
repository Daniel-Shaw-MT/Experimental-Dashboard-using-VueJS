<template>
  <v-col cols="1">
            <v-sheet rounded="lg">
              <v-list color="transparent">
    
        <v-list-item class="" v-for="person in people" :key="person" link>
          <v-tooltip right>
            <template v-slot:activator="{ on, attrs }">
              <v-list-item-content v-bind="attrs" v-on="on">
                <v-avatar outlined color="primary" size="40">
                <span  class="white--text text-h6">{{person.sn}}</span>
                </v-avatar>
                <!-- <v-list-item-title class="ml-2">{{ item.title }} </v-list-item-title> -->
              </v-list-item-content>
            </template>
            <span>{{ person.name }}</span>
          </v-tooltip>
        </v-list-item>

                <v-divider class="my-2"></v-divider>
                <v-list-item link color="grey lighten-4">
                  <v-list-item-content>
                    <v-icon>mdi-refresh</v-icon>
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
        people: [
      {
        name: "Michael Mallia",
        sn: "MM",
        status: "Active"
      },
      {
        name: "Daniel Shaw",
        sn: "DS",
        status: "Active"
      },
      {
        name: "Gianluca Cassar",
        sn: "GC",
        status: "Active"
      },
      {
        name: "Mark Shaw",
        sn: "MS",
        status: "Offline"
      }
    ],
    }),

}
</script>

<style>

</style>