<template>
  <div>
    <v-container fluid>
      <v-row justify="center">
        <v-col cols="10">
          <v-toolbar>
            <v-toolbar-title class="headline font-weight-medium">
              Welcome to the Homepage
            </v-toolbar-title>
          </v-toolbar>
          <v-divider class="pa-1" dark/>
          <v-card>
            <v-card-text>
              <div class="body-1">
                This project was created as a playground to help learn the different pieces we are using to develop a UI. As you can see I have created two tabs above, one with your name and one with my name.
                When clicked they will take you to the respective persons page, which right now are currently empty, however they are meant to be a sandbox to learn and put whatever you want on the page. 
              </div>
              <br>
              <div class="body-1">
                On this page (as well as in the README) I will include several links to resources that I use for development as a whole, as well as some specific to the frameworks we are using for this UI. Click on a tile to see their page:
              </div>
              <v-row justify="space-around">
                <v-col cols="5">
                  <v-list two-line>
                    <v-subtitle class="subtitle grey--text font-weight-light">Resources For Everyday Programming</v-subtitle>
                    <v-list-item-group v-for="(source, idx) in common_resources" :key="idx">
                      <v-list-item :href="source.link" target="_" id="resourceitem">
                        <v-list-item-content>
                          <v-list-item-title>{{source.title}}</v-list-item-title>
                          <v-list-item-subtitle>{{source.description}}</v-list-item-subtitle>
                        </v-list-item-content>
                        <v-list-item-action>
                          <v-icon>exit_to_app</v-icon>
                        </v-list-item-action>
                      </v-list-item>
                    </v-list-item-group>
                  </v-list>
                </v-col>
                <v-col cols="5">
                  <v-list two-line>
                    <v-subtitle class="subtitle grey--text font-weight-light">Resources Specific to This Project</v-subtitle>
                    <v-list-item-group v-for="(source, idx) in project_resources" :key="idx" :href="source.link" target="_">
                      <v-list-item :href="source.link" target="_" id="resourceitem">
                        <v-list-item-content>
                          <v-list-item-title>{{source.title}}</v-list-item-title>
                          <v-list-item-subtitle>{{source.description}}</v-list-item-subtitle>
                        </v-list-item-content>
                        <v-list-item-action>
                          <v-icon>exit_to_app</v-icon>
                        </v-list-item-action>
                      </v-list-item>
                    </v-list-item-group>
                  </v-list>
                </v-col>
              </v-row>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>

export default {
  components: {},
  data: () => ({
    common_resources: [
      {
        title: "VS Code",
        link: "https://code.visualstudio.com/",
        description: "OP Text Editor"
      },
      {
        title: "Cmder",
        link: "https://cmder.net/",
        description: "CMD/Terminal Emulator"
      },
      {
        title: "WSL Ubuntu",
        link: "https://docs.microsoft.com/en-us/windows/wsl/install-win10",
        description: "Ubuntu Filesystem on Windows w/o Dualbooting"
      },
      {
        title: "DataGrip",
        link: "https://www.jetbrains.com/datagrip/",
        description: "Fullscale Database IDE"
      },
      {
        title: "SourceTree",
        link: "https://www.sourcetreeapp.com/",
        description: "Git UI"
      },
    ],
    project_resources: [
      {
        title: "Nuxt.js",
        link: "https://nuxtjs.org/",
        description: "Backend/Server Framework"
      },
      {
        title: "Vue.js",
        link: "https://vuejs.org",
        description: "Frontend Framework"
      },
      {
        title: "Vuetify.js",
        link: "https://vuetify.js.com/en/",
        description: "UI Component Framework"
      },
      {
        title: "Axios",
        link: "https://axios.nuxtjs.org/",
        description: "Javascript API Library"
      },
      {
        title: "JavaScript",
        link: "https://www.w3schools.com/js/",
        description: "References for JavaScript Language"
      },
    ]
  })
}
</script>

<style scoped>
#resourceitem:hover {
  background-color: rgba(60, 60, 130, .5);
}

</style>
