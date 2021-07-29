<template>
  <p>Regstration form here</p>
  <button @click="register">Register</button>
</template>

<script>
export default {
  props: ['event'],
  methods: {
    register() {
      // Assuming successful API call to register them

      //Set a flash message to appear on the next page loaded whicjh says
      //'You are successfully registered for ' + this.event.title

      this.$router.push({
        name: 'EventDetails',
        params: { id: this.event.id }
      })
    }
  }
}
</script>
