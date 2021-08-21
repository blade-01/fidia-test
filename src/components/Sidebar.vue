<template>
    <div class="sidebar">
        <div class="sidebar-content">
          <h3><img src="../assets/img/store.png" alt="store"/> Store name <img src="../assets/img/chevron.png" alt="chevron"/></h3>
          <div>
            <div class="sidebar-inner">
              <p><img src="../assets/img/house.png" alt="house"/> Home</p>
              <ul>
                <li class="payments"><img src="../assets/img/payments.png" alt="payments"/> Payments</li>
                <li class="payment-list" v-for="payment in payments" :key="payment">{{ payment }}</li>
              </ul>
              <ul>
                <li><img src="../assets/img/balances.png" alt="balances"/> Balances</li>
                <li><img src="../assets/img/customers.png" alt="customers"/> Customers</li>
                <li><img src="../assets/img/connect-account.png" alt="connect-account"/> Connected accounts</li>
                <li><img src="../assets/img/products.png" alt="products"/> Products</li>
                <li><img src="../assets/img/reports.png" alt="reports"/> Reports</li>
              </ul>
              <ul>
                <li><img src="../assets/img/devs.png" alt="devs"/> Developers</li>
                <li><img src="../assets/img/toggle.png" alt="toggle"/> View test data</li>
                <li><img src="../assets/img/settings.png" alt="settings"/> Settings</li>
              </ul>
            </div>
          </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Sidebar',
  data() {
    return {
      payments: ['Reviews', 'Disputes', 'Top-ups', 'Collected fees', 'Transfers', 'Payouts', 'All transactions'],
    }
  }
}
</script>

<style scoped>
.sidebar {
  position: fixed;
  width: 250px;
  height: 100%;
  top: 0;
  left: -100%;
  padding-top: 1rem;
  background: var(--side-bg);
  color: var(--store-name);
}
.sidebar-content {
  padding: 0 0 0 1rem;
}
.sidebar-content h3 {
  display: flex;
  align-items: center;
  font-size: 16px;
}
.sidebar-content h3 img:last-child {
  margin-left: 0.5rem;
}
.sidebar-inner .payments {
  color: var(--payment-btn);
}
.sidebar-inner p {
  margin: 1.5rem 0 1rem;
}
.sidebar-inner li {
  padding: 0.3rem 0;
  width: 100%;
}
.sidebar-inner ul {
  margin-bottom: 0.5rem;
}
.sidebar-inner img {
  margin-right: 0.5rem;
}
.sidebar-inner .payment-list {
  margin-left: 1.7rem;
}
@media screen and (min-width: 1000px) {
 .sidebar {
   width: 250px;
   left: 0;
   top: 0;
   height: 100%;
 }
}
</style>