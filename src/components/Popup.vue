<template>
    <div class="text-center">
        <v-dialog v-model="dialog" width="500">
           <template v-slot:activator="{ on, attrs }">
              <v-btn color="red" dark v-bind="attrs" v-on="on">
                 Add new project
              </v-btn>
          </template>
          <v-card >
              <v-card-title class="text-h5 red ">
                  <v-icon left>mdi-plus-box-outline</v-icon>
                    new project
              </v-card-title>
              <v-card-text class="black--text mt-4">
                  <v-form class="px-3">
                      <v-text-field label="Title" v-model="title" prepend-icon="mdi-format-title"></v-text-field>
                      <v-textarea label="Information" v-model="content" prepend-icon="mdi-information-outline"></v-textarea>
                      <v-btn flat class="success mx-0 mt-3" @click="submit"> Add Project</v-btn>
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
            content:''
        }
    },
    methods:{
        submit(){
             console.log(this.title,this.content);
        }
    }

}
</script>

<style>

</style>
      <v-dialog max-width="600px">
          <template v-slot:activator="{ on, attrs }">
            <v-btn flat slot="activator" class="success"></v-btn>
              <v-card>
              <v-card-title>
                  <h2>Add a new project</h2>

              </v-card-title>
             </v-card>
           </template>
      </v-dialog>