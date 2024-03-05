<script>
import NavBar from "./components/NavBar";
import FooTer from "./components/FooTer";
import jQuery from 'jquery';
// import bootstrap from 'bootstrap';
global.jQuery = jQuery;
global.$ = jQuery;



export default {
  name: "app",
  components: {
    NavBar,
    FooTer
  },
  data() {
    return {
      show: false,
      username: "abcd",
      userId: "123",
      password: "123456"
    };
  },
  methods: {
    handleClick() {
      this.$router.push({
        path: '/home'
      })
    },
    updateMe() {
      alert();
      console.log("=============")
    },
    deleteMe() {
      // alert();
      console.log("=============")
    }
  }
}


</script>

<style>
@import "~bootstrap/dist/css/bootstrap.css";
</style>






<template>

  <NavBar />
  <div class="continer py-5">
    <h4>Homepage</h4>
    <p>{{ username }}</p>
    <button class="btn btn-primary py-2 px-3 mt-2" @click="updateMe">Click Me </button>
    <button class="btn btn-danger py-2 px-3 mt-2" @click="updateMe">Click Me </button>
  </div>

  <FooTer></FooTer>



</template>
