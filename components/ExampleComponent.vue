<template>
  <v-container fluid>
    <v-row>
      <v-col cols="10">
        <v-card>
          <v-card-title>Here is a title</v-card-title>
          <v-card-text>
            {{randomVar}}
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "ExampleComponent",
  data: () => ({
    randomVar: "Hello, World!"
  }),
  methods: {
    methodOne() {
      return "Hello"
    }
  }
}
</script>

<style scoped>

</style>