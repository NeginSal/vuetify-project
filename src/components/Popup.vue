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
                  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
              </v-card-text>
           </v-card>
        </v-dialog>
    </div>
</template>

<script>
export default {

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