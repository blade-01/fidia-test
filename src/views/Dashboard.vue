<template>
  <div class="dashboard">
    <Sidebar />
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
}
</script>

<style scoped>
.dashboard {
  position: relative;
}
</style>