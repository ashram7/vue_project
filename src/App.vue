<template lang="html">
    <div id="app">
      <WishHeader></WishHeader>
      <WishInput v-on:addWish="addWish"></WishInput>
      <WishList v-bind:propsdata="wishItems"></WishList>
      <WishFooter></WishFooter>
    </div>
</template>
<script>
    import WishHeader from './components/WishHeader.vue'
    import WishInput from './components/WishInput.vue'
    import WishList from './components/WishList.vue'
    import WishFooter from './components/WishFooter.vue'
    export default {
      data() {
        return {
          wishItems: []
        }
      },
      methods: {
        addWish() {
          // 로컬 스토리지에 데이터를 추가하는 로직
        }
      },
      components: {
          'WishHeader': WishHeader,
          'WishInput': WishInput,
          'WishList': WishList,
          'WishFooter': WishFooter
      }
    }
</script>
<style lang="css">
body {
    text-align: center;
    background-color: #f6f6f8;
}
input {
    border-style: groove;
    width: 200px;
}
button {
    border-style: groove;
}
.shadow {
    box-shadow: 5px 10px 10px rgba(0, 0, 0, 0.03);
}
</style>
