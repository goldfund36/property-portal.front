<template>
<div>
  <div class="sec-title">
    <span class="title">FIND NOW YOUR DREAM HOUSE</span>
    <h2>New Property</h2>
  </div>
  <property-card/>
</div>
</template>

<script>
import PropertyCard from "./PropertyCard";
export default {
  name: "PropertyLayout",
  components: {
    PropertyCard
  }
}
</script>

<style scoped>
</style>
