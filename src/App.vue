<template>
  <div class="bonline">
    <billing-page></billing-page>
  </div>
</template>

<script>
import BillingPage from "./components/BillingPage.vue";
export default {
  name: 'App',
  components: {
   BillingPage
  }
}
</script>

<style>
   @import './components/style.css';
</style>
