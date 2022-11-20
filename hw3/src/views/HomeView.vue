<template>
  <div class="home">
    <Header/>
    <h1>This is main page</h1>
    <Post/>
    <button v-on:click="ResetLikes">Reset likes</button>
    <Footer/>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
import Post from '@/components/Post.vue'
export default {
  name: 'HomeView',
  components: {
    Header,
    Footer,
    Post
  },
  data: function () {
    return {

    }
  },

  methods: {
    ResetLikes: function () {
      this.$store.dispatch("ResetLikesAct")
    },
  }
}
</script>
