<template>
  <div>
    <v-container fluid>
      <v-row>
        <v-col cols="12">
          <example-component></example-component>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import ExampleComponent from "../components/ExampleComponent"

export default {
  components: {
    ExampleComponent
  },
  data: () => ({

  })
}
</script>
