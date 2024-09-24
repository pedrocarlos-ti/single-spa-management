<template>
  <div>
    <h2>Order Management</h2>
    <ul>
      <li v-for="order in orders" :key="order.id">
        Order #{{ order.id }} - ${{ order.total }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      orders: [
        { id: 1001, total: 1299 },
        { id: 1002, total: 699 },
        { id: 1003, total: 1499 },
      ],
    };
  },
};
</script>
