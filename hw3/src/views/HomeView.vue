<template>
    <div class="home">
      <Header/>
      <section class="Content">
          <aside class="Aside">
          </aside>
          <main class="Main" id="main">
              <article class="Article" v-for="post in postsList" :key="post.id">
                <Post :post="post"/>
              </article>
          </main>
          <aside class="Aside">
  
          </aside>
      </section>
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
    computed: {
        postsList(){
            return this.$store.state.postsList
        }
    },
    methods: {
        ResetLikes: function () {
            this.$store.dispatch("ResetLikesAct")
        },
    }
  }
  </script>
  
  <style>
  * {
      font-family: 'Courier New', Courier, monospace;
  }
  
  p {
      line-height: 1.25;
  }
  
  ::placeholder {
      color: grey;
  }
  
  div p {
      font-size: 0.925em;
  }
  
  article+section {
      display: flex;
      flex-direction: row;
  }
  
  main>article {
      border-radius: 10px;
      background-color: rgb(220, 220, 220);
      display: flex;
      flex-direction: column;
      margin: 5px;
      padding: 10px;
      width: calc(100vw - 36vw);
  }
  
  h3~p {
      font-size: 1.05em;
  }
  
  .Aside {
      background-color: rgb(220, 220, 220);
      width: 15vw;
      height: auto;
      border-radius: 10px;
  }
  
  .Header {
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
  
  
  .Header :last-child {
      margin-left: auto;
  }
  
  .Login {
      display: flex;
      flex-direction: column;
      font-weight: bold;
      background-color: rgb(220, 220, 220);
      margin-top: 25px;
      margin-right: 15vw;
      margin-left: 15vw;
      text-align: center;
      padding: 10px;
      border-color: red;
      border-radius: 20px;
  }
  
  .UserDate {
      display: flex;
      flex-direction: row;
      align-items: top;
      padding: 5px;
  }
  
  .UserDate :last-child {
      margin-left: auto;
  }
  
  .Account {
      color: rgb(0, 200, 255);
  }
  
  .Content {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      margin-top: 10px;
      margin-bottom: 60px;
  }
  
  .Main {
      display: flex;
      flex-direction: column;
      justify-content: center;
      flex: 1;
      align-items: center;
      position: relative;
  }
  
  .Footer {
      bottom: 0px;
      width: 99vw;
      border-radius: 10px;
      display: flex;
      background-color: rgb(220, 220, 220);
      position: fixed;
      justify-content: center;
  }
  
  .user_icon {
      height: 50px;
      width: 50px;
      padding-right: 10px;
  }
  
  .like {
      height: 30px;
      width: 30px;
  }
  
  .image {
      max-width: 50%;
      max-height: auto;
      align-self: center;
  }
  
  .Posting {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
  }
  
  .PostBody {
      padding-right: 10px;
  }
  
  #Email {
      height: 30px;
      border: none;
  }
  
  #Password {
      margin: 10px;
      height: 30px;
      border: none;
  }
  
  #LoginButton {
      color: white;
      background-color: rgb(32, 70, 139);
      border: none;
      padding: 5px;
      width: 25%;
  }
  
  #LoginHome:hover {
      background-color: yellowgreen;
  }
  
  #AddPost:hover {
      background-color: yellowgreen;
  }
  
  #textarea {
      width: 100%;
      height: 100%;
      resize: none;
  }
  </style>