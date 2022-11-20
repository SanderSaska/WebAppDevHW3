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

<style scoped>

div  {
    font-size: 0.925em;
}

Footer {
    bottom: 0px;
    width: 99vw;
    border-radius: 10px;
    display: flex;
    background-color: rgb(220, 220, 220);
    position: fixed;
    justify-content: center;
}

Header {
    border-radius: 10px;
    font-size: 2em;
    font-weight: bold;
    background-color: rgb(220, 220, 220);
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 10px;
    padding-left: 20px;
}

</style>


