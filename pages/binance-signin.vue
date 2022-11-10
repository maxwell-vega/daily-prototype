<template>
<div>
  <v-card>
    <v-card-title primary-title>
      <v-row justify="center" align="center">
        <span>
          Binance
        </span>
      </v-row>
    </v-card-title>
    <v-card-actions>
      <v-row justify="center" align="center">
        <v-col cols="10">
          <v-text-field
            v-model="apiKey"
            placeholder="Enter your api key here"
          ></v-text-field>
        </v-col>
      </v-row>
    </v-card-actions>
    <v-card-actions>
      <v-row class="mb-4 mt-2" justify="center" align="center">
        <v-btn @click="confirmApiKey" color="yellow">Confirm</v-btn>
      </v-row>
    </v-card-actions>
  </v-card>
</div>
</template>

<script>
export default {
  data () {
    return {
      apiKey: ""
    }
  },
  methods: {
    confirmApiKey() {
      window.localStorage.setItem('apiKey', this.apiKey)
      this.$router.push({ name: 'dashboard' })
    },
  },
}
</script>
