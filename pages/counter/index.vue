<template>
  <section class="container">
    <div>
      <h1>counter index</h1>
      <p>count={{ count }}</p>
      <v-btn class="mx-2" fab dark color="indigo" @click="addCount">
        <v-icon dark>
          mdi-plus
        </v-icon>
      </v-btn>
      <v-btn class="mx-2" fab dark color="pink" @click="removeCount">
        <v-icon dark>
          mdi-minus
        </v-icon>
      </v-btn>
    </div>
  </section>
</template>

<script>
export default {
  computed: {
    count () { return this.$store.state.counter.count }
  },
  methods: {
    addCount () {
      this.$store.commit('counter/increment')
    },
    removeCount () {
      this.$store.commit('counter/decrement')
    }
  }
}
</script>
