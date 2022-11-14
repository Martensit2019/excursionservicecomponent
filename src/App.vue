<template>
  <v-app>
    <v-container>
      <excursion-block />
    </v-container>
  </v-app>
</template>

<script>
import ExcursionBlock from './components/ExcursionBlock.vue'

export default {
  components: { ExcursionBlock },
  name: 'App',
}
</script>
