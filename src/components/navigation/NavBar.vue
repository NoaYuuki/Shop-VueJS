<template>
  <div class="bg-purple-400 p-2 text-center">
    <a div class="hover:bg-purple-500" href="#" @click="changeComponent('player-view')">Shop</a> | 
    <a div class="hover:bg-purple-500" href="#" @click="changeComponent('selection-list')">Mon panier</a>
  </div>
</template>

<script>
export default {
  name: "nav-bar",
  methods: {
    changeComponent(value) {
      this.$emit('change-component', value)
    }
  }
}
</script>

<style>

</style>