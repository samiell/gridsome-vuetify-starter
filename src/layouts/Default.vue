<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" app>
      
    </v-navigation-drawer>
    <v-app-bar app>
    <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title>{{ $static.metadata.siteName }}</v-toolbar-title>
    </v-app-bar>
    <v-content>
      <slot/>
    </v-content>
    <v-footer app>

    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
    }  
  }
}
</script>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>

</style>
