<template>
  <div class="row">
    <navbar/>
    <layer/>
  </div>
</template>

<script>
import navbar from './components/navbar'
import layer from './components/layer'
export default {
  name: 'app',
  components: {
    navbar,
    layer
  }
}
</script>

<style>
#app {
 background-color: #eeeeee
}
</style>
