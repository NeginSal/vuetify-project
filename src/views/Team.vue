<template >
  <div class="team my-3 mx-3" >
    <h1 class="subheading green--text darken-4--text">Team</h1>
    <v-container class="my-5">
      <v-layout row wrap>
        <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
          <v-card flat class="text-center ma-3" color="green lighten-5">
            <v-responsive class="pt-4">
              <v-avatar size="80" class="green">
                <img :src="person.avatar" alt="">
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="subheading green--text darken-4--text">{{person.name}}</div>
              <div class="grey--text  ">{{person.role}}</div>
            </v-card-text>
            <v-card-action>
              <v-btn flat small color="light-green accent-1">
                <v-icon small left>mdi-message-text-outline</v-icon>
                <span>Message</span>
              </v-btn>
            </v-card-action>
          </v-card>
        </v-flex>
      </v-layout>

    </v-container>
  </div>
</template>

<script>
export default {
  data(){
    return{
      team:[
        {name:'Negin', role:'Web developer',avatar:'/card1.jpg'},
        {name:'Ryu', role:'Graphic designer',avatar:'/card2.jpg'},
        {name:'Chun Li', role:'Web developer',avatar:'/card3.jpg'},
        {name:'Gouken', role:'Social media maverick',avatar:'/card4.jpg'},
        {name:'Yoshi', role:'Sales guru',avatar:'/card5.jpg'}
      ]
    }
  }
}
</script>

<style>
</style>