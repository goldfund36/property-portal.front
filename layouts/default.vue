<template>
  <div>
    <TopBanner/>
    <navbar/>
    <div class="container pt-5">
       <Nuxt />
    </div>
  </div>
</template>

<script>
import Navbar from "../components/Navbar";
import TopBanner from "../components/TopBanner";
export default {
  components: {
    Navbar,
    TopBanner
  }
}
</script>
<style>
body {
  font-family: 'Roboto Condensed', sans-serif;
}
</style>
