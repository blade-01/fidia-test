<template>
    <div class="mainbar">
      <Searchbar />
      <PayButtons />
      <Table />
    </div>
</template>

<script>
import PayButtons from '@/components/PayButtons.vue'
import Searchbar from '@/components/Searchbar.vue'
import Table from '@/components/Table.vue'
export default {
  name: 'Mainbar',
  components: {
    Table, 
    PayButtons, 
    Searchbar
  },
}
</script>

<style scoped>
.mainbar {
  background: var(--card-bg);
  height: 100%;
  border-left: solid 1px var(--store-bg);
}
@media screen and (min-width: 1000px) {
 .mainbar {
   margin-left: 250px;
   z-index: 100;
 }
}
</style>