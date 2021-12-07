<template>
  <v-dialog max-width="600" :value="$store.state.hardRefresh" persistent>
    <v-card>
      <v-card-title>Update available</v-card-title>
      <v-card-text>
        New GUI update available please do a hard refresh to load latest changes.
        <br>
        <br>
        Mac users : <kbd>cmd</kbd> + <kbd>shift</kbd> + <kbd>R</kbd>
        <v-divider vertical class="mx-3" />
        Other users : <kbd>ctrl</kbd> + <kbd>shift</kbd> + <kbd>R</kbd>
        <br>
        <br>

        Or press following button <v-btn x-small outlined @click="reload">
          Reload
        </v-btn>
      </v-card-text>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  name: 'HardRefreshModal',
  methods: {
    reload() {
      window.location.reload(true)
    }
  }

}
</script>

<style scoped>

</style>
