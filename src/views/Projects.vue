<template>
  <div class="project my-3 mx-3">
    <h1 class="blue--text text--darken-4">This is Projects page</h1>
    <v-container class="my-5">
      <v-row justify="center">
        <v-expansion-panels accordion>
          <v-expansion-panel>
            <v-expansion-panel-header>Project title</v-expansion-panel-header>
            <v-expansion-panel-content>
              <v-card flat>
                <v-card-text class="px-4 blue--text">
                  <div class="font-weight-bold">duo by xx.xx.xx</div>
                  <div>info</div>
                </v-card-text>
              </v-card>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-row>
    </v-container>
  </div>
</template><script>
  export default {
    data(){
      return{

      }
    }
  }
</script>



