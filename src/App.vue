<template>
  <div>
    <navbar v-on:click-tutorial="showtutorial" v-on:click-blog="showblog" v-on:click-home="showhome"></navbar>
    <blog v-if="blogshown"></blog>
    <tutorial v-if="tutorialshown"></tutorial>
    <home v-if="homeshown"></home>
    <pagefooter></pagefooter>
  </div>
</template>

<script>
import home from './components/home.vue'
import navbar from './components/navbar.vue'
import blog from './components/blog.vue'
import tutorial from './components/tutorial.vue'
import pagefooter from './components/pagefooter.vue'

export default {
  name: 'App',
  components: {
    home,
    navbar,
    blog,
    tutorial,
    pagefooter
  },
  data () {
    return {
      tutorialshown:false,
      blogshown:false,
      homeshown:true,

    }
  },
  methods: {
    showtutorial() {
      if (this.tutorialshown == true) {
        this.tutorialshown = false;
        this.blogshown = false;
        this.homeshown = true;
      }
      else if (this.tutorialshown == false) {
        this.tutorialshown = true;
        this.blogshown = false;
        this.homeshown = false;
      }
    },
    showblog() {
      if (this.blogshown == true) {
        this.tutorialshown = false;
        this.blogshown = false;
        this.homeshown = true;
      }
      else if (this.blogshown == false) {
        this.blogshown = true;
        this.tutorialshown = false;
        this.homeshown = false;
      }
    },
    showhome() {
      if (this.homeshown == false) {
        this.tutorialshown = false;
        this.blogshown = false;
        this.homeshown = true;
      }
    }
  }
}

</script>

<style>

</style>
