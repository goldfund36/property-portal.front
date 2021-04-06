<template>
  <section>
    <h1>My profile {{ $auth.user.name }}</h1>
  </section>

</template>

<script>
export default {
  name: "index",
  middleware: 'auth'
}
</script>

<style scoped>

</style>
