<template>
  <div class="container">
    <h2>Order Management</h2>
    <table class="order-table">
      <thead>
        <tr>
          <th>Order ID</th>
          <th>Total Amount</th>
          <th>Customer Name</th>
          <th>Order Date</th>
          <th>Actions</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="order in orders" :key="order.id">
          <td>{{ order.id }}</td>
          <td>${{ order.total }}</td>
          <td>{{ order.customerName }}</td>
          <td>{{ order.orderDate }}</td>
          <td>
            <button @click="viewOrder(order.id)">View</button>
            <button @click="editOrder(order.id)">Edit</button>
            <button @click="deleteOrder(order.id)">Delete</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      orders: [
        {
          id: 1001,
          total: 1299,
          customerName: "John Doe",
          orderDate: "2023-01-01",
        },
        {
          id: 1002,
          total: 699,
          customerName: "Jane Smith",
          orderDate: "2023-01-02",
        },
        {
          id: 1003,
          total: 1499,
          customerName: "Alice Johnson",
          orderDate: "2023-01-03",
        },
        {
          id: 1004,
          total: 899,
          customerName: "Bob Brown",
          orderDate: "2023-01-04",
        },
        {
          id: 1005,
          total: 1999,
          customerName: "Charlie Davis",
          orderDate: "2023-01-05",
        },
        {
          id: 1006,
          total: 299,
          customerName: "Diana Evans",
          orderDate: "2023-01-06",
        },
      ],
    };
  },
  methods: {
    viewOrder(id) {
      alert(`Viewing order ${id}`);
    },
    editOrder(id) {
      alert(`Editing order ${id}`);
    },
    deleteOrder(id) {
      alert(`Deleting order ${id}`);
    },
  },
};
</script>

<style scoped>
.container {
  text-align: center;
  background-color: #ffffff;
  padding: 20px;
}

h2 {
  color: #333;
  margin-bottom: 20px;
  text-align: left;
}

.order-table {
  width: 100%;
  border-collapse: collapse;
  margin: 20px 0;
}

.order-table th,
.order-table td {
  border: 1px solid #ddd;
  padding: 8px;
}

.order-table th {
  background-color: #07a;
  color: white;
  text-align: left;
}

.order-table tr:nth-child(even) {
  background-color: #f2f2f2;
}

.order-table tr:hover {
  background-color: #ddd;
}

.order-table th {
  padding-top: 12px;
  padding-bottom: 12px;
  text-align: left;
  background-color: #07a;
  color: white;
}

button {
  margin: 0 5px;
  padding: 8px 12px;
  background-color: #07a;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #057;
}
</style>
