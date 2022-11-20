<template>
  <Header/>
  <form class="Signup" @submit.prevent="submitForm" v-if="!formSubmitted">
      <span>Email</span><br>
      <input
        v-model="Email"
        type="email"
        placeholder="Email"
      /><br>
      <span>Password</span><br>
      <input
        v-model="Password"
        type="password"
        placeholder="Password"
      /><br>
      <button>Signup</button>
  </form>
  <Footer/>
</template>

<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'


export default {
  name: 'HomeView',
  components: {
    Header,
    Footer
  }
}


</script>

<style scoped>

Footer {
    bottom: 0px;
    width: 99vw;
    border-radius: 10px;
    display: flex;
    background-color: grey;
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

.Signup {
    display: flex;
    flex-direction: column;
    color: white;
    background-color: rgb(32, 70, 139);
    border: none;
    padding: 20px;
    width: 25%;
    align-items: center;
    margin-left: auto;
    margin-right: auto;
}


</style>
