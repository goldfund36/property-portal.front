<template>
  <div class="row">
    <div class="col-6 offset-3">
      <h1>Login page</h1>
      <b-form @submit.prevent="submit">
        <b-form-group
          id="input-group-1"
          label="Email address:"
          label-for="input-1"
        >
          <b-form-input
            id="input-1"
            type="email"
            v-model="email"
            placeholder="Enter email"
            required
          ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-2" label="Your password:" label-for="input-2">
          <b-form-input
            id="input-2"
            type="password"
            placeholder="Enter password"
            v-model="password"
            required
          ></b-form-input>
        </b-form-group>

        <b-button type="submit" variant="danger">Send</b-button>
      </b-form>
    </div>
  </div>
</template>

<script>
export default {
  name: "login",
  data() {
    return {
      email: '',
      password: ''
    }
  },
  methods: {
    submit() {
      this.$auth.loginWith('laravelJWT',
        {
          data: {
            email: this.email,
            password: this.password
          }
        })
        .then(() => this.$router.push({ path: '/profile' }))

    }
  },
  mounted() {
    if(this.$auth.loggedIn) {
      this.$router.push({ path: '/profile' })
    }
  }
}
</script>

<style scoped>

</style>
