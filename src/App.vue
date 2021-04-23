<template>
  <v-app>
    <v-navigation-drawer app color="#00BCD4"> </v-navigation-drawer>

    <v-app-bar app color="#00BCD4" class="white--text">
      <v-toolbar-title>Request Man</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-avatar color="#03A9F4" size="56">
        <v-icon dark> mdi-account-circle </v-icon>
      </v-avatar>
    </v-app-bar>

    <v-main>
      <v-container fluid>
        <router-view></router-view>
      </v-container>
    </v-main>

  </v-app>
</template>

<script>
export default {
  name: 'App',
};
</script>
