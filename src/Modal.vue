<template>
  <div class="black-bg" v-if="모달창 == true" >
    <div class="white-bg">
      <img :src="원룸들[누른거]?.image" class="room-img">
      <h4>{{원룸들[누른거].title}}</h4>
      <h4>{{원룸들[누른거].content}}</h4>
      <h4>{{원룸들[누른거].price}}원</h4>
      <Discount/>
       <!-- <button class="xx" @click="모달창 = false">X</button> -->
      </div>
      </div>

</template>

<script>
import Discount from './Discount.vue'

export default {
    name: "Modal",
    props:{
        원룸들: Array,
        모달창: Boolean,
        누른거: Number
    },
  components: {
     Discount
  },

}
</script>

<style>

</style>