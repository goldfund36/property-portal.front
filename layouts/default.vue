<template>
  <div>
    <navbar/>
    <div class="container pt-5">
       <Nuxt />
    </div>
  </div>
</template>

<script>
import Navbar from "../components/Navbar";
export default {
  components: {Navbar}
}
</script>
<style>
body {
  font-family: 'Roboto Condensed', sans-serif;
}
</style>
