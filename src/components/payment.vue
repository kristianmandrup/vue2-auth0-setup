<template>
  <div id='App'>
    <h1>Please give us your payment details:</h1>
    <card class='stripe-card'
      :class='{ complete }'
      :stripe='stripeKey'
      :options='stripeOptions'
      @change='complete = $event.complete'
    />
    <button class='pay-with-stripe' @click='pay' :disabled='!complete'>Pay with credit card</button>
  </div>
</template>

<script>
import { stripeKey, stripeOptions } from './stripeConfig.json'
import { Card, createToken } from 'vue-stripe-elements'

export default {
  date () {
    return { complete: false }
  },

  components: { Card },

  methods: {
    pay () {
      createToken().then(data => console.log(data.token))
    }
  }
}
</script>

<style>
.stripe-card {
  width: 300px;
  border: 1px solid grey;
}
.stripe-card.complete {
  border-color: green;
}
</style>