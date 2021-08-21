<template>
  <router-view></router-view>
</template>

<script>
export default {
  name: 'App',
}
</script>

<style>
body {
  font-family: -apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Ubuntu,sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 15px;
  color: var(--pri-color);
}
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
:root {
  --bg: #F7FAFC;
  --side-bg: #F7FAFC;
  --store-bg: #E5E5E5;
  --card-bg: #FFFFFF;
  --pri-color: #697386;
  --sec-color: #635CFF;
  --title-color: #3C4257;
  --btn: #635CFF;
  --payment-btn: #5469D4;
  --copy-tab: #697386;
  --store-name: #1A1F36;
  --current-tab: #5469D4;
  --success: #CBF4C9;
  --tab-desc: #4F566B;
  --results: #3C4257;
}
.box-shadow {
    box-shadow: 0 2px 2px 0 rgba(0, 0, 0, 0.14), 0 3px 1px -2px rgba(0, 0, 0, 0.12), 0 1px 5px 0 rgba(0, 0, 0, 0.2);
}
.btn-shadow {
    box-shadow: 0 3px 3px 0 rgba(0, 0, 0, 0.14), 0 1px 7px 0 rgba(0, 0, 0, 0.12), 0 3px 1px -1px rgba(0, 0, 0, 0.2);
}
.btn {
  border: none;
  outline: none;
  background: transparent;
}
.container {
  width: 90%;
  margin: auto;
  overflow: hidden;
}
button {
  cursor: pointer;
}
a {
  text-decoration: none;
  color: var(--sec-color);
}
input {
  outline: none;
  border: solid 1px #ddd;
  padding: 0.8rem 1rem;
  border-radius: 5px;
}
label {
  color: var(--title-color);
}
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
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
