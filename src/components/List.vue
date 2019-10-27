<template>
  <v-app>
    <v-content>
      <v-container class="fill-height" fluid>
        <v-row align="center" justify="center">
          <v-col cols="10" sm="8" md="4">
            <v-card class="elevation-8">
              <v-toolbar color="primary" dark flat>
                <v-title>Your Habit Reports</v-title>
                <v-spacer></v-spacer>
              </v-toolbar>
              <v-layout justify-center>
                <v-card class="d-inline-block mx-auto">
                  <v-card class="mx-auto" min-width="300" tile>
                    <v-list class="elevation=0" flat>
                      <v-subheader>Triggers</v-subheader>
                      <v-list-item-group v-model="itemA" color="primary">
                        <v-list-item v-for="(itemA, i) in itemsA" :key="i">
                          <template v-slot:default="{ active, toggle }">
                            <v-list-item-action>
                              <v-checkbox v-model="active" color="primary" @click="toggle"></v-checkbox>
                            </v-list-item-action>
                            <v-list-item-content>
                              <v-list-item-title v-text="itemA.text"></v-list-item-title>
                            </v-list-item-content>
                          </template>
                        </v-list-item>
                      </v-list-item-group>
                    </v-list>
                    <v-list flat>
                      <v-subheader>Routines</v-subheader>
                      <v-list-item-group v-model="itemB" color="primary">
                        <v-list-item v-for="(itemB, i) in itemsB" :key="i">
                          <template v-slot:default="{ active, toggle }">
                            <v-list-item-action>
                              <v-checkbox v-model="active" color="primary" @click="toggle"></v-checkbox>
                            </v-list-item-action>
                            <v-list-item-content>
                              <v-list-item-title v-text="itemB.text"></v-list-item-title>
                            </v-list-item-content>
                          </template>
                        </v-list-item>
                      </v-list-item-group>
                    </v-list>
                    <v-list flat>
                      <v-subheader>Rewards</v-subheader>
                      <v-list-item-group v-model="itemC" color="primary">
                        <v-list-item v-for="(itemC, i) in itemsC" :key="i">
                          <template v-slot:default="{ active, toggle }">
                            <v-list-item-action>
                              <v-checkbox v-model="active" color="primary" @click="toggle"></v-checkbox>
                            </v-list-item-action>
                            <v-list-item-content>
                              <v-list-item-title v-text="itemC.text"></v-list-item-title>
                            </v-list-item-content>
                          </template>
                        </v-list-item>
                      </v-list-item-group>
                    </v-list>
                  </v-card>
                </v-card>
              </v-layout>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>



<script>
export default {
  props: {
    source: String
  },
  data: () => ({
    itemA: 1,
    itemsA: [
      { text: "Whatever it causes you" },
      { text: "Daily Active" },
      { text: "Prizes" }
    ],
    itemB: 1,
    itemsB: [{ text: "FUCK YOU" }, { text: "FUCK YOU TOO" }, { text: "WHAT?" }],
    itemC: 1,
    itemsC: [
      { text: "LICK ME" },
      { text: "KISS MY ASS" },
      { text: "BLOW IT OFF" }
    ]
  })
};
</script>