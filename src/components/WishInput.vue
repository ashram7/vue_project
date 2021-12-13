<!-- WishInput.vue -->
<template lang="html">
  <div class="inputBox shadow">
    <input type="text" v-model="newWishItem" v-on:keyup.enter="addWish"
        placeholder="Type what you wish to do">
    <span class="addContainer" v-on:click="addWish">
      <i class="addBtn fas fa-plus" aria-hidden="true"></i>
    </span>
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
input:focus {
  outline: none;
}
.inputBox {
  background: white;
  height: 50px;
  line-height: 50px;
  border-radius: 5px;
  margin-bottom: 25px;
}
.inputBox input {
  border-style: none;
  font-size: 1.2em;
  font-weight: bold;
  width: 12em;
  color: #2f3b52;
}
.addContainer {
  float: right;
  background: linear-gradient(to right, #ff4c4d, #b30000);
  display: inline-block;
  width: 3em;
  border-radius: 0 5px 5px 0;
}
.addBtn {
  color: white;
  vertical-align: middle;
}
</style>
