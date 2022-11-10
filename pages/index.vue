<template>
<div>
  <v-row justify="center" align="center">
    <span>
      Your Wallet
    </span>
  </v-row>
  <v-row class="mt-6" justify="center" align="center">
    <v-btn @click="clickBinance" color="yellow">Binance</v-btn>
  </v-row>
  <v-row class="mt-6" justify="center" align="center">
    <v-btn color="blue">Coinbase</v-btn>
  </v-row>
  <v-row class="mt-6" justify="center" align="center">
    <v-btn color="orange">MetaMask</v-btn>
  </v-row>
    <!-- <v-col cols="12">
    </v-col> -->
</div>
</template>

<script>
export default {
  name: 'IndexPage',
  methods: {
    clickBinance () {
      this.$router.push({ name: 'binance-signin' })
    },
  },
}
</script>
