<template>
<div>
  <h2 class="text-center mb-4">Best property in Alanya</h2>
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
