<template>
    <div class="text-center">
        <v-dialog v-model="dialog" width="500">
           <template v-slot:activator="{ on, attrs }">
              <v-btn color="red" dark v-bind="attrs" v-on="on">
                 Add new project
              </v-btn>
          </template>
          <v-card >
              <v-card-title class="text-h5 blue-grey lighten-2 ">
                  <v-icon left>mdi-plus-box-outline</v-icon>
                    new project
              </v-card-title>
              <v-card-text class="black--text mt-4">
                  <v-form class="px-3">
                      <v-text-field label="Title" v-model="title" prepend-icon="mdi-format-title"></v-text-field>
                      <v-textarea label="Information" v-model="content" prepend-icon="mdi-information-outline"></v-textarea>

                      <v-menu>
                        <template v-slot:activator="{ on, attrs }">
                            <v-text-field v-model="date" label="Duo date" prepend-icon="mdi-calendar"
                                readonly v-bind="attrs" v-on="on">
                            </v-text-field>
                        </template>
                        <v-date-picker v-model="date" @input="menu2 = false"></v-date-picker>
                      </v-menu>
                      <v-btn flat class="blue-grey lighten-2 mx-0 mt-3" @click="submit"> Add Project</v-btn>
                  </v-form>

              </v-card-text>
           </v-card>
        </v-dialog>
    </div>
</template>

<script>
export default {
    data(){
        return{
            title:'',
            content:'',
            menu2: false,

        }
    },
    methods:{
        submit(){
             console.log(this.title,this.content);
        },

    }

}
</script>

<style>

</style>
