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
          // 인풋 박스의 입력 값이 있을 때만 저장
          if(this.newWishItem !== ""){
            // 인풋 박스에 입력된 텍스트의 앞뒤 공백 문자열 제거
            var value = this.newWishItem && this.newWishItem.trim();
            //console.log(this.newWishItem);
            //localStorage.setItem(this.newWishItem, this.newWishItem);
            localStorage.setItem(value, value);
            // 인풋 박스의 입력 값을 초기화
            this.clearInput();
          }
        },
        clearInput(){
          this.newWishItem = '';
        }        
      }
    }
</script>
<style lang="css" scoped>
</style>
