<!-- WishList.vue -->
<template lang="html">
  <section>
    <ul>
      <li>위시리스트 1</li>
      <li>위시리스트 2</li>
      <li>위시리스트 3</li>
      <li>위시리스트 4</li>
      <li>위시리스트 5</li>
    </ul>
  </section>
</template>
<script>
    export default {
      data() {
        return {
          wishItems: []
        }
      },
      created() {
        if (localStorage.length > 0) {
          for (var i = 0; i < localStorage.length; i++) {
            this.wishItems.push(localStorage.key(i));
          }
        }
      }      
    }
</script>
<style lang="css" scoped>
</style>
