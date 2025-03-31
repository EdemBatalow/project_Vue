<template>
  <v-app>
    <v-navigation-drawer app></v-navigation-drawer>

    <v-app-bar app dark color="primary">
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-spacer></v-spacer>

      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn>
          <v-icon start>mdi-cake-variant</v-icon> <!-- Здесь используется встроенная иконка Vuetify -->
          Link One
        </v-btn>

        <v-btn>
          <v-icon start>mdi-cupcake</v-icon>  <!-- Можно использовать другие иконки -->
          Link Two
        </v-btn>

        <v-btn> 
          <v-icon start>mdi-cake-layered</v-icon>
          Link Three
        </v-btn>
      </v-toolbar-items>
    </v-app-bar>

    <v-main>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
     
    }
  }
}
</script>
