<template>
  <div class="dashboard">
    <div @click="openNav"
          class="hamburger"
          :class="{ change: open }">
      <div></div>
      <div></div>
      <div></div>
    </div>
    <div class="sidebar" :class="{ open: open }">
      <Sidebar />
    </div>    
    <Mainbar />
  </div>
</template>

<script>
import Sidebar from '@/components/Sidebar.vue'
import Mainbar from '@/components/Mainbar.vue'
export default {
  name: 'Dashboard',
  components: {
    Sidebar,
    Mainbar,
  },
  data() {
    return {
      open: false,
    }
  },
  methods: {
    openNav() {
      this.open = !this.open;
    }
  }
}
</script>

<style scoped>
.dashboard {
  position: relative;
}
.hamburger {
  background: var(--payment-btn);
  position: fixed;
  bottom: 15px;
  right: 15px;
  padding: 0.5rem;
  border-radius: 50%;
  z-index: 100;
}
.hamburger > div {
  height: 2px;
  width: 20px;
  background: var(--card-bg);
  margin: 0.2rem 0;
  transition: transform ease-in-out 0.4s;
}
.change.hamburger > div:nth-child(1) {
  transform: translate(1px, 5px) rotate(45deg);
}
.change.hamburger > div:nth-child(2) {
  opacity: 0;
}
.change.hamburger > div:nth-child(3) {
  transform: translate(0px, -6px) rotate(-45deg);
}
.sidebar {
  position: fixed;
  width: 250px;
  height: 100%;
  top: 0;
  left: -100%;
  padding-top: 1rem;
  background: var(--side-bg);
  color: var(--store-name);
  z-index: 10;
  transition: ease-in-out 0.4s left;
}
.open.sidebar {
  left: 0;
}
@media screen and (min-width: 1000px) {
  .hamburger {
    display: none;
  }
  .sidebar {
   width: 250px;
   left: 0;
   top: 0;
   height: 100%;
 }
}
</style>