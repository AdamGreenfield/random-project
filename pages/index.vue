<template>
  <div>
    <v-container fluid>
      <v-row>
        <v-col cols="12">
          <example-component></example-component>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12">
          <modal></modal>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import ExampleComponent from "../components/ExampleComponent"
import Modal from "../components/Modal"

export default {
  components: {
    ExampleComponent,
    Modal
  },
  data: () => ({

  })
}
</script>
