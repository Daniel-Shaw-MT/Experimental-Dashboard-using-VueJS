<template>
    <v-col>
            <v-sheet min-height="54vh" rounded="lg">
              <v-list color="transparent">
                <v-list-item color="grey lighten-4">
                  <v-list-item-content>
                    <v-list-item-title>Lessons up next</v-list-item-title>
                  </v-list-item-content>
                 </v-list-item>
                <v-divider class="my-2"></v-divider>
                <v-list-item class="" v-for="lesson in lessons" :key="lesson">
                  <v-list-item-content class="pa-3">
                    <v-card class="pa-1" elevation="1" shaped tile>
                      <v-col>
                      <v-sheet>
                        
                          <v-list-item-title class="ml-2"
                        >{{ lesson.title }}
                        <v-text class="pr-1">{{ lesson.TS }}</v-text>
                        
                        <v-text >{{ lesson.TE }}</v-text>
                      </v-list-item-title>
                                                
                      <v-list-item-subtitle class="ml-2">{{
                        lesson.account
                      }}</v-list-item-subtitle>
                      <v-list-item-subtitle class="ml-2">{{
                        lesson.text
                      }}</v-list-item-subtitle>
                      <v-sheet class="pa-2"> </v-sheet>
                      <v-card-actions>
                        <!-- <v-btn><v-icon>mdi-thumb-up</v-icon></v-btn>
                        <v-btn><v-icon>mdi-thumb-down</v-icon></v-btn>
                        <v-btn><v-icon>mdi-export-variant</v-icon></v-btn> -->
                        <v-btn small><v-icon>mdi-send</v-icon></v-btn>
                        <v-spacer></v-spacer>
                        <v-btn small><v-icon>mdi-arrow-right</v-icon></v-btn>
                      </v-card-actions>


                        </v-sheet>
                        
                        </v-col>
                        
                        
                      
                      
                      
                      <!-- <v-card-actions class="justify-end">
                      
                    </v-card-actions>
                       -->
                    </v-card>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </v-sheet>
          </v-col>
</template>

<script>
export default {
    beforeMount() {
    this.getLessons();
    },
    methods: {
        getLessons: function() {
            fetch("http://localhost:8000/getAposts")
        .then((response) => response.json())
        .then((data) => (this.lessons = data))
        .catch((error) => console.log(error));
        }
    },
    data: () => ({
        lessons: [],

    })
}
</script>

<style>

</style>