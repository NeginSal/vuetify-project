<template>
<div class="dashboard my-3 mx-3">
  <h1 class="subheading purple--text  lighten-1--text">Dashboard</h1>
  <v-container class="my-5">
    <v-layout row class="mb-3">
      <v-tooltip top>
      <template v-slot:activator="{ on, attrs }">
      <v-btn small flat class="ml-5 mr-3" color="gray" @click="sortBy('title')" v-bind="attrs" v-on="on">
        <v-icon small left >mdi-file-document-edit-outline</v-icon>
        <span class="caption text-lowercase">By project name</span>
      </v-btn>
      </template>
      <span>Sort projects by name</span>
      </v-tooltip>
      <v-tooltip top>
      <template v-slot:activator="{ on, attrs }">
      <v-btn small flat color="gray" @click="sortBy('person')" v-bind="attrs" v-on="on">
        <v-icon small left >mdi-account-edit-outline</v-icon>
        <span class="caption text-lowercase">By persom</span>
      </v-btn>
      </template>
      <span>Sort projects by person</span>
      </v-tooltip>
    </v-layout>

    <v-card flat class="pa-3 ma-2 purple lighten-5" v-for="project in projects" :key="project.title">
      <v-layout row wrap :class="`pa-3 project ${project.status}`">
        <v-flex xs12 md6>
          <div class="caption purple--text">Project Title</div>
          <div>{{project.title}}</div>
        </v-flex>
        <v-flex xs6 sm4 md2>
          <div class="caption purple--text">Person</div>
          <div>{{project.person}}</div>
        </v-flex>
        <v-flex xs6 sm4 md2>
          <div class="caption purple--text">Duo by</div>
          <div>{{project.due}}</div>
        </v-flex>
        <v-flex xs2 sm4 md2>
          <div >
            <v-chip id="chip" small :class="`${project.status} white--text caption my-2`">{{project.status}}</v-chip>
          </div>
        </v-flex>
      </v-layout>
    </v-card>
  </v-container>
</div>


</template>

<script>
  export default {
    data(){
      return{
        projects:[
          {title:'create a new website', person:'Negin', due:'30 june 2021', status:'ongoing'},
          {title:'Code up the homepage', person:'Chun Li', due:'10 july 2021', status:'complete'},
          {title:'Design Video tumbnails', person:'Ryu', due:'20 Sep 2021', status:'complete'},
          {title:'Create a Cummunity forum', person:'Guken', due:'10 Oct 2021', status:'overdue'},
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
<style scoped>
   .project.complete{
     border-left: 4px solid #00cc00;
   }
   .project.ongoing{
     border-left: 4px solid #0099ff;
   }
   .project.overdue{
     border-left: 4px solid #ff0000;
   }
  #chip.v-chip.complete {
     background: #00cc00;
   }
   #chip.v-chip.ongoing{
     background: #0099ff;

   }
   #chip.v-chip.overdue{
    background: #ff0000;
   }
</style>