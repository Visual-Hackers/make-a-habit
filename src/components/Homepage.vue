<template>
  <v-container>
    <v-stepper v-model="e1">
      <v-stepper-header>
        <v-stepper-step 
          :complete = "e1 > 1" 
          color ="#43a047" 
          step="1">Trigger
        </v-stepper-step>
        <v-divider></v-divider>
        <v-stepper-step 
          :complete = "e1 > 2" 
          color ="#43a047" 
          step="2">Routine
        </v-stepper-step>
        <v-divider></v-divider>
        <v-stepper-step 
          :complete = "el > 3" 
          color ="#43a047" 
          step="3">Reward
        </v-stepper-step>
      </v-stepper-header>
      <v-stepper-items>
        <v-stepper-content step="1">
          <v-card
            class="mb-12"
            color="#FFFF"
            height="44px">
            <v-text-field
              v-model="describe"
              :rules="describeRules"
              label="What object or technique will you use as a trigger?"
              required>
            </v-text-field>
          </v-card>
          <v-btn
            color="#a6f1a6"
            @click="e1=2">Next Step
          </v-btn>
        </v-stepper-content>
        <v-stepper-content step="2">
          <v-card
            class="mb-12"
            color="#FFFF"
            height="44px">
            <v-text-field
              v-model="describe"
              :rules="describeRules"
              label="What are the details of your routine?"
              required>
            </v-text-field>
          </v-card>
          <v-btn
            color="#a6f1a6"
            @click="e1 = 3">Continue
          </v-btn>
        </v-stepper-content>
        <v-stepper-content step="3">
          <v-card
            class="mb-12"
            color="#FFF"
            height="44px">
            <v-text-field
              v-model="describe"
              :rules="describeRules"
              label="What's your reward?"
              required>
            </v-text-field>
          </v-card>
          <v-btn
            color="#a6f1a6"
            @click="e1 = 1">Continue
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
          v => !!v || 'Required',
          v => /./.test(v) || 'Must be valid',
        ]
      }
    }
  }
</script>
