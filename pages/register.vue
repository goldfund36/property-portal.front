<template>
  <div class="row">
    <div class="col-6 offset-3">
      <h1>Register</h1>
      <b-form @submit.prevent="submit">
        <b-form-group
          id="input-group-1"
          label="Email address:"
          label-for="input-1"
        >
          <b-form-input
            id="input-1"
            type="email"
            placeholder="Enter email"
            v-model="email"
            required
          ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-2" label="Your Name:" label-for="input-2">
          <b-form-input
            id="input-2"
            v-model="name"
            placeholder="Enter name"
            required
          ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-2" label="Your password:" label-for="input-2">
          <b-form-input
            id="input-2"
            type="password"
            v-model="password"
            placeholder="Enter password"
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
  name: "register",
  data() {
    return {
        email: '',
        name: '',
        password: ''
    }
  },
  methods: {
    submit() {
        this.$axios.post('/api/auth/register',{
          email: this.email,
          name: this.name,
          password: this.password
        }).then((response) => {
            if(typeof response.data.access_token !== undefined) {
              this.$auth.setUserToken(response.data.access_token,true);
              this.$router.push({ path: '/profile' })
            }
        })
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
