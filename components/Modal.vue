<template>
    <v-row justify="center">
          <v-dialog v-model="dialog" persistent max-width="300">
            <template v-slot:activator="{ on }">
              <v-btn color="primary" dark v-on="on">Create Account</v-btn>
            </template>
            <v-card>
              <v-card-title>Create Account</v-card-title>
              <v-card-text>
                <v-form>
                  <v-container>
                    <v-row>
                      <v-col cols="12">
                        <v-text-field label="Username"></v-text-field>
                      </v-col>
                    </v-row>
                    <v-row>
                      <v-col cols="12">
                        <v-text-field label="Password"></v-text-field>
                      </v-col>
                    </v-row>
                  </v-container>
                </v-form>
              </v-card-text>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn text @click="dialog = false">Submit</v-btn>
                <v-btn text @click="reset">Cancel</v-btn>
              </v-card-actions>
            </v-card>
          </v-dialog>
    </v-row>
</template>


<script>
  export default {
    name: "Modal",
    data: () => ({
      dialog: false
    }),
    methods: {
      reset(){
        this.$refs.form.reset()
      }
    }
  }
</script>
