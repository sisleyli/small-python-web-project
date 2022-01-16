<template>
  <div id="app" class="">
    <onnx-manage/>
  </div>
</template>

<script>
import OnnxManage from './components/OnnxManage.vue'

export default {
  name: 'App',
  components: {
    OnnxManage
  }
}
</script>

<style scoped>
.whole-container{
  height: 100vh;
  width: 100vw;
}
</style>
