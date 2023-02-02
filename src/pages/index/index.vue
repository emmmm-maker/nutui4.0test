<template>
  <nut-steps :current="current1">
    <nut-step title="填写信息">
      1
    </nut-step>
    <nut-step title="拍摄照片">2</nut-step>
    <nut-step title="签约刷脸支付">3</nut-step>
  </nut-steps>
</template>

<script lang="ts">
import { reactive, toRefs } from 'vue'
import { Dongdong } from '@nutui/icons-vue-taro'
export default {
  name: 'Index',
  components: {
    Dongdong
  },
  setup() {
    const state = reactive({
      current1: 1,
    })
    const handleClickStep = (index: number) => {
      console.log(index)
    }
    return { ...toRefs(state), handleClickStep }
  }
}
</script>

<style lang="scss">
.index {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
