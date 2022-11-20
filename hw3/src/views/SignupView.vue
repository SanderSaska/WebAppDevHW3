<template>
  <Header/>
  <div class="signup">
    <h1>This is signup page</h1>
  </div>
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
