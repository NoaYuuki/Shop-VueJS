<template>
  <div class="border-double border-4 border-purple-600 text-center bg-purple-200 rounded m-4 p-4">
    Panier : {{ selection.length }}
    <span v-if="numberSelection">article</span>
    <span v-else>articles</span>

    <ul>
      <li v-for="joueur in selection" :key="joueur.name">{{ joueur.name }}</li>
    </ul>

  </div>
  
</template>

<script>
export default {
  name: "selection-box",
  props: ['selection'],
  computed: {
    numberSelection(){
      if(this.selection.length < 2){
        return true
      }
      return false
    }
  }

}
</script>

<style>

</style>