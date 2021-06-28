<template>
  <nav>
<!--Navigation-drawer-->
    <v-navigation-drawer app v-model="drawer" class="deep-orange lighten-4" >
      <v-list>
        <v-list-item v-for="link in links" :key="link.text" router :to="link.route">
          <v-list-item-action>
            <v-icon class="red--text text--darken-4" large>{{link.icon}}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-tile-title class="red--text text--darken-4">{{link.text}}</v-list-tile-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
<!--Navigation-drawer-->
<!--Toolbar-->
    <v-app-bar app color="orange lighten-4">
        <v-app-bar-nav-icon @click.stop="drawer = !drawer" color="deep-orange darken-4"></v-app-bar-nav-icon>
        <v-toolbar flat app color="orange lighten-4">
            <v-toolbar-title class="text-uppercase deep-orange--text text--darken-4">
                Vuetify Site
                <v-icon color="deep-orange accent-4"> mdi-heart </v-icon>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn flat color="orange darken-1">
                <span>Sign Out</span>
                <v-icon right>mdi-logout</v-icon>
            </v-btn>
        </v-toolbar>
    </v-app-bar>
  </nav>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    drawer: false,
    links: [
      {icon: 'mdi-view-dashboard' ,text:'Dashboard', route: '/'},
      {icon: 'mdi-folder-open' ,text:'My Projects', route: '/projects'},
      {icon: 'mdi-human-greeting' ,text:'Team', route: '/team'},

    ]

  })
}
</script>
<style>
</style>