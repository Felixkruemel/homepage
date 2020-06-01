<template>
  <div>
    <navbar></navbar>
    <home></home>
  </div>
</template>

<script>
import home from './components/home.vue'
import navbar from './components/navbar.vue'

export default {
  name: 'App',
  components: {
    home,
    navbar
  }
}
</script>

<style>

</style>
