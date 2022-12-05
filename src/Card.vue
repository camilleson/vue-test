<template>
    <div> 
    <img :src="원룸들.image" class="room-img">
    <h4 @click="$emit('openModal',  원룸들.id)">{{원룸들.title}}</h4> 
    <h4>{{원룸들.content}}</h4>
    <p> {{원룸들.price}} $</p>
  </div>
</template>

<script>
export default {
    name:"Card",
    props:{
        원룸들: Array,
    },
}
</script>

<style>

</style>