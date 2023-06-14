<template>
  <div className="column is-3">
    <div className="box">
      <figure className="image mb-4">
        <img v-bind:src="product.get_thumbnail">
      </figure>

      <h3 className="is-size-4">{{ product.name }}</h3>
      <p className="is-size-6 has-text-grey">${{ product.price }}</p>

      <router-link v-bind:to="product.get_absolute_url" className="button is-dark mt-4">View details</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductBox',
  props: {
    product: Object
  }
}
</script>

<style scoped>
.image {
  margin-top: -1.25rem;
  margin-left: -1.25rem;
  margin-right: -1.25rem;
}
</style>