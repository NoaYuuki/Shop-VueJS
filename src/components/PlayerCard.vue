<template>
  <div class="border bg-purple-100 m-2 p-2 flex justify-between rounded">
    <div>
      <h1 class="text-lg font-bold">{{ playerName }}</h1>
      <p> {{ playerPositionUp }} </p>
    </div>
    <base-button
      text="Ajouter"
      @click="addToSelection"
    >
    </base-button>
  </div>
</template>

<script>
export default {
  name: "player-card",
  props: ['player'],
  computed: {
    playerName(){
      if(this.player.name.split('.').length > 1){
        return this.player.name.split('.')[1]
      }
      return this.player.name;
    },
    playerPositionUp(){
      return this.player.position.toUpperCase()
    }
  },
  methods: {
    addToSelection() {
      this.$emit('add-player', this.player)
    }
  }
}
</script>

<style scoped>

</style>