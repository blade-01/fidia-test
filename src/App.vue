<template>
  <sign-up />
  <div class="container">
  </div>
</template>

<script>
import SignUp from './components/signUp.vue'

export default {
  name: 'App',
  components: {
    SignUp
  }
}
</script>

<style>
body {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 15px;
}
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.box-shadow {
    -webkit-box-shadow: 0 2px 2px 0 rgba(0, 0, 0, 0.14), 0 3px 1px -2px rgba(0, 0, 0, 0.12), 0 1px 5px 0 rgba(0, 0, 0, 0.2);
    box-shadow: 0 2px 2px 0 rgba(0, 0, 0, 0.14), 0 3px 1px -2px rgba(0, 0, 0, 0.12), 0 1px 5px 0 rgba(0, 0, 0, 0.2);
}
.btn-shadow {
    -webkit-box-shadow: 0 3px 3px 0 rgba(0, 0, 0, 0.14), 0 1px 7px 0 rgba(0, 0, 0, 0.12), 0 3px 1px -1px rgba(0, 0, 0, 0.2);
    box-shadow: 0 3px 3px 0 rgba(0, 0, 0, 0.14), 0 1px 7px 0 rgba(0, 0, 0, 0.12), 0 3px 1px -1px rgba(0, 0, 0, 0.2);
}
.container {
  width: 90%;
  margin: auto;
  overflow: hidden;
}
a {
  text-decoration: none;
}
input {
  outline: none;
  border: solid 1px gray;
  padding: 0.8rem 1rem;
  border-radius: 5px;
}
@media screen and (min-width: 700px) {
  .container {
    width: 80%;
  }
}
@media screen and (min-width: 1000px) {
  .container {
    width: 968px;
  }
}
@media screen and (min-width: 1200px) {
  .container {
    width: 1100px;
  }
}
</style>
