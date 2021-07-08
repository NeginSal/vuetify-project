<template>
  <div class="project my-3 mx-3">
    <h1 class="blue--text text--darken-4">This is Projects page</h1>
    <v-container class="my-5">
      <v-row justify="center">
        <v-expansion-panels >
          <v-expansion-panel  v-for="project in projects" :key="project.title">
            <v-expansion-panel-header class="cyan--text text--darken-4">{{project.title}}</v-expansion-panel-header>
            <v-expansion-panel-content>
              <v-card flat color="blue lighten-4">
                <v-card-text class="px-4">
                  <div class="font-weight-bold blue--text">duo by {{project.duo}}</div>
                  <div class="teal--text text--darken-4">{{project.content}}</div>
                </v-card-text>
              </v-card>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-row>
    </v-container>
  </div>
</template>

<script>
  export default {
    data(){
      return{
        projects:[
          {title:'create a new website', person:'Negin', due:'30 june 2021', status:'ongoing',content:'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'},
          {title:'Code up the homepage', person:'Chun Li', due:'10 july 2021', status:'complete',content:'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'},
          {title:'Design Video tumbnails', person:'Ryu', due:'20 Sep 2021', status:'complete',content:'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'},
          {title:'Create a Cummunity forum', person:'Guken', due:'10 Oct 2021', status:'overdue',content:'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'},
        ]
      }
    },
    methods: {
      sortBy(prop){
        this.projects.sort((a,b) => a[prop] < b[prop] ? -1 : 1)
      }
    }
  }
</script>



