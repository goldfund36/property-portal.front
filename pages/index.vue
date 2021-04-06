<template>
  <div>
    <h1 class="text-center mb-3">Поиск недвижимости в Турции</h1>
      <property-filter/>
    <property-layout/>
  </div>
</template>

<script>
import PropertyFilter from "../components/PropertyFilter";
import PropertyLayout from "../components/PropertyLayout";
export default {
  components: {
    PropertyFilter,
    PropertyLayout
  }
}
</script>

<style>

</style>
