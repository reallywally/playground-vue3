<template>
  <div>

  </div>
</template>

<script>
import {reactive, ref} from "vue";

export default {
  setup() {
    const count = ref(0)
    const state = reactive({
      count,
    })

    count.value++
    count.value++

    console.log(count.value)
    console.log(state.count)  // count 자체는 ref로 감싸져있지만 value로 접근하지 않아도 된다.

    return {

    }
  }
}
</script>

<style scoped>

</style>