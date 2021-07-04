<template>
  <div class="project pa-3">
    <div class="mb-5">
      <h1>Project</h1>
    </div>

    <v-container>
      <v-layout row class="mb-3">
        <v-tooltip top>
          <template v-slot:activator="{ on }">
            <v-btn v-on="on" text color="grey" @click="sortBy('title')">
              <v-icon>mdi-folder</v-icon>
              <span class="caption text-lowercase">by project name</span>
            </v-btn>
          </template>
          <span>Order list by project name</span>
        </v-tooltip>
        <v-tooltip top>
          <template v-slot:activator="{ on }">
            <v-btn v-on="on" text color="grey" @click="sortBy('name')">
              <v-icon>mdi-account</v-icon>
              <span class="caption text-lowercase">by person name</span>
            </v-btn>
          </template>
          <span>Order list by person name</span>
        </v-tooltip>
      </v-layout>
      <v-layout row>
        <v-flex v-for="project in projects" :key="project.name" xs6 md3 lg3>
          <v-card class="pa-3 ma-2">
            <div class="caption text-break">{{ project.title }}</div>
            <div>{{ project.name }}</div>
            <div>
              <v-chip dark class="pink lighten-2" small>ongoing</v-chip>
            </div>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>
<script>
export default {
  data: () => {
    return {
      projects: [
        { name: "Feryadi", title: "Create website e-commerce" },
        { name: "Adi Andoyo", title: "Create website Sistem Informasi" },
        { name: "Willy", title: "Create website company profile" },
        { name: "Kevin", title: "Create website social media" },
        { name: "Hendri Januardi", title: "Create website job vacancy" },
        { name: "Willy Yanpraga", title: "Create website landing page" },
        { name: "Reinaldo Putra", title: "Create website food order" },
        { name: "Velzen", title: "Create website streaming" },
        { name: "Chalvin", title: "Create website email" }
      ]
    };
  },
  methods: {
    sortBy(props) {
      this.projects.sort((a, b) => (a[props] < b[props] ? -1 : 1));
    }
  }
};
</script>