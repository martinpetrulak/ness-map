<template>
  <v-app>
    <v-navigation-drawer
      persistent
      :mini-variant="miniVariant"
      v-model="drawer"
      enable-resize-watcher
      fixed
      app
    >
      <v-list>
        <v-list-tile to="/">
          <v-list-tile-action>
            <v-icon>home</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Home</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile to="/routing">
          <v-list-tile-action>
            <v-icon>navigation</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Routing</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile to="/advanced-routing">
          <v-list-tile-action>
            <v-icon>navigation</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Advanced Routing</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile to="/heatmap">
          <v-list-tile-action>
            <v-icon>map</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Ness KE Employees</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile to="/places">
          <v-list-tile-action>
            <v-icon>place</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Places</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <!-- <v-list-tile to="/weather">
          <v-list-tile-action>
            <v-icon>cloud</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Weather</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile> -->
      </v-list>
    </v-navigation-drawer>
    <v-toolbar dark app color="blue darken-3"
    >
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-btn icon @click.stop="miniVariant = !miniVariant">
        <v-icon v-html="miniVariant ? 'chevron_right' : 'chevron_left'"></v-icon>
      </v-btn>
      <v-toolbar-title v-text="title"></v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>
    <v-content>
      <router-view/>
    </v-content>
    <v-footer fixed dark app color="blue darken-3" class="pa-3">
      <div>Ness Map &copy; 2017</div>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      drawer: false,
      miniVariant: false,
      title: 'Ness Map'
    }
  },
  name: 'App'
}
</script>
