<!-- WishFooter.vue -->
<template lang="html">
  <div class="clearAllContainer">
    <span class="clearAllBtn" @click="clearWish">Clear All</span>
  </div>
</template>
<script>
    export default {
      methods: {
        clearWish() {
          this.$emit('removeAll');
        }
      }
    }
</script>
<style lang="css" scoped>
.clearAllContainer{
    width: 7.5em;
    height: 50px;
    line-height: 50px;
    background: linear-gradient(to right, #ff4c4d, #b30000);
    border-radius: 5px;
    margin: 25px auto 0px;
}
.clearAllBtn{
    font-weight: bold;
    text-transform: uppercase;
    letter-spacing: -1px;
    color: white;
    display: block;
}
</style>
