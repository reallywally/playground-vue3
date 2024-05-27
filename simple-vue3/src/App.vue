<template>
  <div>
    <h2>반응형 counter</h2>
    <p>{{count}}</p>
    <button @click="addCount">+</button>

    <h2>노말 counter</h2>
    <p>{{normalCount}}</p>
    <button @click="addNormalCount">+</button>
  </div>
</template>

<script>
import {ref} from "vue";

export default {
  setup(){
    // 반응형
    const count = ref(0)
    const addCount = () => {
      count.value++
    }

    //노멀
    let normalCount = 0
    const addNormalCount = () => {
      normalCount++
    }

    return {
      count,
      addCount,
      normalCount,
      addNormalCount
    }
  }
}
</script>



<style scoped>

</style>
