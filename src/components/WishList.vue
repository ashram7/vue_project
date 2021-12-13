<!-- WishList.vue -->
<template lang="html">
  <section>
    <ul>
      <li v-for="wishItem in wishItems"> {{ wishItem }} </li>
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
