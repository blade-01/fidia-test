<template>
      <div class="padded">
        <div class="table-tab">
          <h2>Payments</h2>
          <div class="buttons">
            <button class="btn btn-shadow"><img src="../assets/img/filter.png" alt="filter"/> Filter</button>
            <button class="btn btn-shadow"><img src="../assets/img/export.png" alt="export"/> Export</button>
            <button class="btn btn-shadow"><img src="../assets/img/plus.png" alt="plus"/> Create payment</button>
          </div>
        </div>
      </div>
</template>

<script>
export default {
  name: 'PayButtons',
}
</script>

<style scoped>
.buttons {
  display: flex;
  justify-content: space-between;
  margin-top: 1rem;
}
.padded {
  padding: 0 1rem;
}
.table-tab {
  margin: 0.5rem auto;
}
.table-tab h2 {
  font-size: 30px;
  color: var(--store-name);
}
.buttons .btn {
  padding: 0.5rem 0.8rem;
  border: solid 1px var(--store-bg);
  outline: none;
  border-radius: 3px;
  background: var(--card-bg);
  display: flex;
  align-items: center;
  color: var(--results);
}
.buttons .btn img {
  margin-right: 0.3rem;
}
.buttons .btn:last-child {
  background: var(--payment-btn);
  border: none;
  color: var(--card-bg);
}
@media screen and (min-width: 500px) {
  .table-tab {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 1rem;
  }
  .buttons {
    margin: 0;
  }
  .buttons button {
    margin-left: 0.5rem;
  }
}
</style>