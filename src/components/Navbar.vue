<template>
  <nav>
    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="text-upercase grey--text">
        <span class="font-weight-light">Todo</span>
        <span>Ninja</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn fab small text color="grey">
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
      <v-btn text color="grey">
        <v-icon>mdi-exit-to-app</v-icon>
        <span>Sign out</span>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer app v-model="drawer" class="pink white--text">
      <v-list>
        <v-list-item v-for="drawer in drawerList" :key="drawer.title" router :to="drawer.route">
          <v-list-item-icon>
            <v-icon class="white--text">{{ drawer.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="white--text">{{ drawer.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>
<script>
export default {
  data: () => {
    return {
      drawer: null,
      drawerList: [
        {
          icon: "mdi-view-dashboard",
          title: "Dashboard",
          route: "/"
        },
        {
          icon: "mdi-folder",
          title: "Folder",
          route: "project"
        },
        {
          icon: "mdi-account",
          title: "Person",
          route: "team"
        }
      ]
    };
  }
};
</script>