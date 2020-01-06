<template>
  <v-app dark>
    <v-app-bar fixed app>
      <v-toolbar-title>Random Project</v-toolbar-title>
      <v-spacer />
      <v-toolbar-items>
        <template v-for="(tab, index) in tabs">
          <v-hover :key="index">
            <v-btn slot-scope="{ hover }" :to="tab.to" :key="tab.title" text
              :class="`font-weight-medium subheading elevation-${hover ? 12 : 0}`">
              <v-icon color="secondary">{{tab.icon}}</v-icon>&nbsp;{{tab.title}}
            </v-btn>
          </v-hover>
        </template>
      </v-toolbar-items>
    </v-app-bar>
    <v-content>
      <v-container fluid>
        <nuxt />
      </v-container>
    </v-content>
    <v-footer :fixed="fixed" app>
      <span>&copy; 2019</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      tabs: [
        {
          icon: "home",
          title: "Home",
          to: "/"
        },
        {
          icon: 'accessible',
          title: "Stephen's Page",
          to: '/stephen'
        },
        {
          icon: 'pregnant_woman',
          title: "Cole's Page",
          to: '/cole'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
