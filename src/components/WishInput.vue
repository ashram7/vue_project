<!-- WishInput.vue -->
<template lang="html">
    <div>
      <input type="text" v-model="newWishItem">
      <button v-on:click="addWish">추가</button>
    </div>
</template>
<script>
    export default {
      data(){
        return {
          newWishItem:''
        }
      },
      methods:{
        addWish(){
          //console.log(this.newWishItem);
          localStorage.setItem(this.newWishItem, this.newWishItem);
        }
      }
    }
</script>
<style lang="css" scoped>
</style>
