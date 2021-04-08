<template>
  <div>
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
h2 {
  position: relative;
  display: block;
  font-size: 30px;
  line-height: 1.2em;
  color: #1a1d1f;
  font-weight: 700;
  text-transform: uppercase;
}
.sec-title {
  position: relative;
  padding-left: 30px;
  margin-bottom: 20px;
  margin-top: 60px;
}
.sec-title .title {
  position: relative;
  display: block;
  font-size: 15px;
  color: #00a75e;
  font-weight: 700;
  top: -4px;
  text-transform: uppercase;
  margin-bottom: 6px;
}
</style>
