<template>
<div>
  <v-card>
    <v-card-title primary-title>
      <v-row justify="center" align="center">
        <span>
          Dashboard
        </span>
      </v-row>
    </v-card-title>
    <!-- <v-card-actions>
      <v-row justify="center" align="center">
        <v-col cols="10">
          <v-text-field
            v-model="apiKey"
            placeholder="Enter your api key here"
          ></v-text-field>
        </v-col>
      </v-row>
    </v-card-actions> -->
  </v-card>
</div>
</template>

<script>
export default {
  name: 'DashboardView',
  data () {
    return {
    }
  },
  mounted () {
    this.$axios.defaults.headers.common = {
      "X-MBX-APIKEY": window.localStorage.getItem('apiKey')
    }
    this.$axios('/sapi/v1/capital/config/getall')
      .then(({ status, data }) => console.log(status, data))
  },
  methods: {
  },
}
</script>
