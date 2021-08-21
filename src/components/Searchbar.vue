<template>
  <div class="dash-field">
    <form class="search-field">
      <input type="text" placeholder="Search..." />
      <img src="../assets/img/search.png" alt="search"/>
    </form>
    <div class="icons">
      <img src="../assets/img/notification.png" alt="notification"/>
      <img src="../assets/img/help.png" alt="help"/>
      <img src="../assets/img/account.png" alt="account"/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Searchbar',
}
</script>

<style scoped>
.dash-field {
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: solid 1px var(--store-bg);
  padding: 0.5rem 1rem;
}
.search-field {
  position: relative;
}
.search-field input {
  width: 100%;
  height: 100%;
  display: block;
  border: none;
  outline: none;
  padding: 0.8rem 1.5rem;
  z-index: 100;
  border-radius: 0;
  transition: ease-in-out 0.4s border;
}
.search-field input:focus {
  border-bottom: solid 1px var(--sec-color);
}
.search-field img {
  position: absolute;
  top: 50%;
  left: 0px;
  transform: translate(0%, -50%);
}
.dash-field .icons {
  display: flex;
  justify-content: space-between;
}
.dash-field .icons img {
  margin-left: 0.5rem;
}
</style>