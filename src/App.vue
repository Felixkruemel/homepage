<template>
  <div>
    <navbar v-on:click-tutorial="showtutorial" v-on:click-blog="showblog"></navbar>
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
  },
  data () {
    return {
      tutorialshown:false,
      blogshown:false,
    }
  },
  methods: {
    showtutorial() {
      if (this.tutorialshown == true) {
        this.tutorialshown == false;
        this.blogshown == false;
      }
      else if (this.tutorialshown == false) {
        this.tutorialshown == true;
        this.blogshown == false;
      }
    },
    showblog() {
      if (this.blogshown == true) {
        this.tutorialshown == false;
        this.blogshown == false;
      }
      else if (this.blogshown == false) {
        this.blogshown == true;
        this.tutorialshown == false;
      }
    }
  }
}

</script>

<style>

</style>
