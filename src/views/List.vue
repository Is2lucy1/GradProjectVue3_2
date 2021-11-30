<template>

  <div class="List">
    <div class="row justify-content-center">
        <div class="col-md-5">
            <h3 class="text-center">Subscriptions</h3>
              <table class="table align-middle">
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Description</th>
                        <th>Amount</th>
                        <th>Actions</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="subscription in subscriptions" :key="subscription.id">
                        <td>{{ subscription.title }}</td>
                        <td>{{ subscription.description }}</td>
                        <td>{{ subscription.amount }}</td>
<!--                        <td>-->
<!--                            <router-link :to="{name: 'edit', params: { id: subscription.key }}" class="btn btn-primary">Edit-->
<!--                            </router-link>-->
<!--                            <button @click.prevent="deleteSubscription(subscription.key)" class="btn btn-danger">Delete</button>-->
<!--                        </td>-->
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
  </div>
</template>

<script>


export default {
  name: "List",
  data() {
    return {
      subscriptions: [
        {
          id: '1',
          title: 'Netflix',
          description: 'video/show streaming',
          amount: 15.69
        }
      ]
    }
  }
}
</script>

<style scoped>
.table {
  width: 100%;
  border-collapse: collapse;
}

.table td,.table th {
  padding: 12px 15px;
  border: 1px solid #ddd;
  text-align:center;
}


</style>
