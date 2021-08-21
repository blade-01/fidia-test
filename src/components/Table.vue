<template>
  <div class="padded">
    <ul class="tabs">
    <li>all</li>
    <li>suceeded</li>
    <li>refunded</li>
    <li>uncaptured</li>
    </ul>
    <table class="table">
      <thead>
        <tr>
          <th><input type="checkbox" /></th>
          <th>amount</th>
          <th></th>
          <th>description</th>
          <th></th>
          <th>customer</th>
          <th>date</th>
          <th></th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="table in tables" :key="table">
          <td><input type="checkbox" /></td>
          <td data-label="Amount">{{ table.amount }}</td>
          <td data-label=" "><span class="success">{{ table.status }} <img src="../assets/img/check.png" alt="check"/></span></td>
          <td data-label="Description">{{ table.desc }}</td>
          <td data-label=" "></td>
          <td data-label="Customer">{{ table.customer }}</td>
          <td data-label="Date">{{ table.date }}</td>
          <td>...</td>
        </tr>
      </tbody>
    </table>
    <div class="counter">
      <p><span class="number">{{tables.length}}</span> results</p>
      <div class="paginate">
        <button class="btn">Previous</button>
        <button class="btn">Next</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Table',
    data() {
    return {
      tables: [
        {
          amount: 'US$352.22',
          status: 'Succeeded',
          desc: 'fe3d216-5819-4dc1-aef-2f19463b5258',
          customer: 'hefovo87@ereyemind.com',
          date: '7 Jul, 14:04',
        },
        {
          amount: 'US$352.22',
          status: 'Succeeded',
          desc: 'fe3d216-5819-4dc1-aef-2f19463b5258',
          customer: 'hefovo87@ereyemind.com',
          date: '7 Jul, 14:04',
        },
        {
          amount: 'US$352.22',
          status: 'Succeeded',
          desc: 'fe3d216-5819-4dc1-aef-2f19463b5258',
          customer: 'hefovo87@ereyemind.com',
          date: '7 Jul, 14:04',
        },
        {
          amount: 'US$352.22',
          status: 'Succeeded',
          desc: 'fe3d216-5819-4dc1-aef-2f19463b5258',
          customer: 'hefovo87@ereyemind.com',
          date: '7 Jul, 14:04',
        },
        {
          amount: 'US$352.22',
          status: 'Succeeded',
          desc: 'fe3d216-5819-4dc1-aef-2f19463b5258',
          customer: 'hefovo87@ereyemind.com',
          date: '7 Jul, 14:04',
        },
        {
          amount: 'US$352.22',
          status: 'Succeeded',
          desc: 'fe3d216-5819-4dc1-aef-2f19463b5258',
          customer: 'hefovo87@ereyemind.com',
          date: '7 Jul, 14:04',
        },
        {
          amount: 'US$352.22',
          status: 'Succeeded',
          desc: 'fe3d216-5819-4dc1-aef-2f19463b5258',
          customer: 'hefovo87@ereyemind.com',
          date: '7 Jul, 14:04',
        },
        {
          amount: 'US$352.22',
          status: 'Succeeded',
          desc: 'fe3d216-5819-4dc1-aef-2f19463b5258',
          customer: 'hefovo87@ereyemind.com',
          date: '7 Jul, 14:04',
        },
        {
          amount: 'US$352.22',
          status: 'Succeeded',
          desc: 'fe3d216-5819-4dc1-aef-2f19463b5258',
          customer: 'hefovo87@ereyemind.com',
          date: '7 Jul, 14:04',
        },
        {
          amount: 'US$352.22',
          status: 'Succeeded',
          desc: 'fe3d216-5819-4dc1-aef-2f19463b5258',
          customer: 'hefovo87@ereyemind.com',
          date: '7 Jul, 14:04',
        },
        {
          amount: 'US$352.22',
          status: 'Succeeded',
          desc: 'fe3d216-5819-4dc1-aef-2f19463b5258',
          customer: 'hefovo87@ereyemind.com',
          date: '7 Jul, 14:04',
        },
        {
          amount: 'US$352.22',
          status: 'Succeeded',
          desc: 'fe3d216-5819-4dc1-aef-2f19463b5258',
          customer: 'hefovo87@ereyemind.com',
          date: '7 Jul, 14:04',
        },
        {
          amount: 'US$352.22',
          status: 'Succeeded',
          desc: 'fe3d216-5819-4dc1-aef-2f19463b5258',
          customer: 'hefovo87@ereyemind.com',
          date: '7 Jul, 14:04',
        },
        {
          amount: 'US$352.22',
          status: 'Succeeded',
          desc: 'fe3d216-5819-4dc1-aef-2f19463b5258',
          customer: 'hefovo87@ereyemind.com',
          date: '7 Jul, 14:04',
        },
        {
          amount: 'US$352.22',
          status: 'Succeeded',
          desc: 'fe3d216-5819-4dc1-aef-2f19463b5258',
          customer: 'hefovo87@ereyemind.com',
          date: '7 Jul, 14:04',
        },
        {
          amount: 'US$352.22',
          status: 'Succeeded',
          desc: 'fe3d216-5819-4dc1-aef-2f19463b5258',
          customer: 'hefovo87@ereyemind.com',
          date: '7 Jul, 14:04',
        },
      ],
    }
  }
}
</script>

<style scoped>
.padded {
  padding: 0 1rem;
}
.table {
   width: 100%;
   border-collapse: collapse;
   color: var(--store-name);
}
.table thead tr th {
  font-size: 14px;
  font-weight: medium;
  letter-spacing: 0.35px;
  color: var(--store-name);
  padding: 12px 8px;
  vertical-align: top;
  border-top: 1px solid var(--store-bg);
  border-bottom: 1px solid var(--store-bg);
  opacity: 1;
  text-transform: uppercase;
  text-align: left;
}
.table tbody tr td:nth-child(2) {
   color: var(--title-color);
   font-weight: bold;
}
.table tbody tr td .success {
  background: var(--success);
  color: #0E6245;
  border: solid 1px #0E6245;
  border-radius: 5px;
  padding: 5px;
}
.table tbody tr td {
  font-size: 14px;
  letter-spacing: 0.35px;
  font-weight: normal;
  color: var(--tab-desc);
  padding: 12px 8px;
  text-align: left;
  border-top: 1px solid var(--store-bg);
  border-bottom: 1px solid var(--store-bg);
}
.table td:nth-child(4) {
  color: var(--tab-desc);
}
.table td:nth-child(6),
.table td:nth-child(7) {
  color: var(--title-color);
}
.counter {
  margin: 1rem 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.counter p {
  color: var(--results);
}
.counter span.number {
  font-weight: 500;
}
.counter .paginate .btn {
  margin-left: 0.5rem;
  padding: 0.5rem 1rem;
  border-radius: 5px;
  border: solid 1px var(--store-bg);
}
.counter .paginate .btn:first-child {
  color: var(--pri-color);
}
ul.tabs {
  margin: 1.5rem 0 0;
}
ul.tabs li{
  display: inline-block;
  margin-right: 1.5rem;
  text-transform: capitalize;
  cursor: pointer;
}
ul.tabs li:nth-child(2) {
  color: var(--payment-btn);
  border-bottom: solid 2px var(--payment-btn);
  padding-bottom: 0.5rem;
}
@media screen and (max-width: 768px) {
  .padded {
    padding: 0.5rem 1rem 0;
  }
  .table thead {
    display: none;
  }
  .table, .table tbody, .table tr, .table td {
    display: block;
    width: 100%;
  }
  .table tr {
    margin-bottom: 15px;
  }
  .table tbody tr td {
    text-align: right;
    padding-left: 40%;
    position: relative;
    border: solid 1px var(--store-bg);
  }
  .table thead tr th {
    border: solid 1px var(--store-bg);
  }
  .table td::before {
    content: attr(data-label);
    position: absolute;
    left: 0;
    width: 60%;
    padding-left: 15px;
    font-weight: 600;
    font-size: 14px;
    text-align: left;
  }
  .table td:nth-child(1)::before {
    content: 'Check';
  }
  .table td:nth-child(3)::before {
    content: 'Status';
  }
}
</style>