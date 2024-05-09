<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
      color="#1679AB"
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <template v-slot:append>
        <div class="pa-2">
          <v-btn block to="/"> Logout </v-btn>
        </div>
      </template>
    </v-navigation-drawer>

    <v-app-bar :clipped-left="clipped" fixed
     app color="#074173">
 
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />

      <v-spacer />
    </v-app-bar>

    <v-main>
      <Nuxt />
    </v-main>

    <v-footer>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      rightDrawer: false,
      right: true,
      clipped: true,
      miniVariant: false,
      items: [
        { title: "Home", icon: "mdi-home", to: "/dashboard" },
        { title: "StudentList", icon: "mdi-account-box", to: "/StudentList" },
        { title: "About", icon: "mdi-information", to: "/about" },
        { title: "Account", icon: "mdi-account", to: "/account" },
        

      ],
    };
  },
};
</script>
