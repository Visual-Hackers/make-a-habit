<template>
  <v-container>
    <!-- <v-row justify="space-around">
        <v-btn fab dark large color="orange" x-large = "300">
          <span class="white--text headline">Habit</span>
        </v-btn>
    </v-row> -->
    <!-- <v-row justify="center">
    <v-dialog v-model="dialog" fullscreen hide-overlay transition="dialog-bottom-transition">
      <template v-slot:activator="{ on }">
        <v-btn color="primary" dark v-on="on">Trigger</v-btn>
      </template>
      <v-card>
        <v-toolbar dark color="primary">
          <v-btn icon dark @click="dialog = false">
            <v-icon>mdi-close</v-icon>
          </v-btn>
          <v-toolbar-title>Trigger</v-toolbar-title>
          <v-spacer></v-spacer>
          <v-toolbar-items>
            <v-btn dark text @click="dialog = false">Save</v-btn>
          </v-toolbar-items>
        </v-toolbar>
        <v-list three-line subheader>
          <v-subheader>Trigger >> Routine >> Reward</v-subheader>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>Pick the words that describle the object</v-list-item-title>
              <v-list-item-subtitle>........................</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>What to represent</v-list-item-title>
              <v-list-item-subtitle>...........................</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-list>
        <v-divider></v-divider>
      </v-card>
    </v-dialog>
  </v-row> -->
  <v-stepper v-model="e1">
    <v-stepper-header>
      <v-stepper-step :complete="e1 > 1" color ="#43a047" step="1">Trigger</v-stepper-step>
      <v-divider></v-divider>
      <v-stepper-step :complete="e1 > 2" color ="#43a047" step="2">Routine</v-stepper-step>
      <v-divider></v-divider>
      <v-stepper-step color ="#43a047" step="3">Reward</v-stepper-step>
    </v-stepper-header>
    <v-stepper-items>
      <v-stepper-content step="1">
        <v-card
          class="mb-12"
          color="#FFFF"
          height="44px"
        >
        <v-text-field
            v-model="describe"
            :rules="describeRules"
            label="What is your necessary for trigger?"
            required
          ></v-text-field>
        </v-card>
        <v-btn
          color="#a6f1a6"
          @click="e1 = 2"
        >
          Continue
        </v-btn>
      </v-stepper-content>
      <v-stepper-content step="2">
        <v-card
          class="mb-12"
          color="#FFFF"
          height="44px"
        >
        <v-text-field
            v-model="describe"
            :rules="describeRules"
            label="Can you explain your routine?"
            required
          ></v-text-field>
        </v-card>
        <v-btn
          color="#a6f1a6"
          @click="e1 = 3"
        >
          Continue
        </v-btn>
      </v-stepper-content>
      <v-stepper-content step="3">
        <v-card
          class="mb-12"
          color="#FFFF"
          height="44px"
        >
        <v-text-field
            v-model="describe"
            :rules="describeRules"
            label="What's your reward?"
            required
          ></v-text-field>
        </v-card>
        <v-btn
          color="#a6f1a6"
          @click="e1 = 1"
        >
          Continue
        </v-btn>
      </v-stepper-content>
    </v-stepper-items>
  </v-stepper>
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
        dialog: false,
        notifications: false,
        sound: true,
        widgets: false,
        e1: 0,
        valid: false,
        describe: '',
        describeRules: [
        v => !!v || 'describe is required',
        v => /./.test(v) || 'describe must be valid',
      ],
      }
    },
  }
</script>

<style scoped>

</style>