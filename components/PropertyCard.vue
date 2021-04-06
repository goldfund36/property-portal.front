<template>
  <div class="row">
    <div class="col-md-4 col-12 mb-1" v-for="i of 18">
      <b-card
        title="Best property for sale in Alanya"
        img-src="/images/estate1.jpg"
        img-alt="Image"
        img-top
        tag="article"
        class="mb-2"
      >
        <b-card-text>
          <div class="row">
            <div class="col-md-6">
              Square: 178
            </div>
            <div class="col-md-6">
              Rooms: 15
            </div>
          </div>
        </b-card-text>

        <div class="row">
          <div class="col-md-8">
            <a href="#">BestPropertyCompany</a>
          </div>
          <div class="col-md-4">
            <a href="#">Read more</a>
          </div>
        </div>
      </b-card>
    </div>
  </div>
</template>

<script>
export default {
  name: "PropertyCard"
}
</script>

<style scoped>

</style>
