<template>
  <div class="container w-4/5 mx-auto mt-4">
    <h1 class="text-lg font-bold">Mon panier</h1>

    <div v-if="selection.length == 0">
      <p>Aucun article dans le panier</p>
    </div>
    <div v-else>
      <div
        v-for="player in selection"
        :key="player.name" 
        class="border border-white flex items-center bg-purple-200 my-4 p-4">
        <img class="p-4 h-25 w-40" :src="require('../assets/img/' + player.photo)" alt="">
        <h3 class="">{{ player.name }} ({{ player.number }})</h3>  
      </div>
    </div>
  </div>
  
</template>

<script>
export default {
  name: "selection-list",
  props: ['selection'],
}
</script>

<style>

</style>