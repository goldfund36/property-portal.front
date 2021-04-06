<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="success">
      <div class="container">
        <nuxt-link to="/"><b-navbar-brand>Portal</b-navbar-brand></nuxt-link>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <b-nav-item-dropdown right v-if="isAuthenticated">
              <!-- Using 'button-content' slot -->
              <template #button-content>
                <em>{{ loggedInUser.name }}</em>
              </template>
              <nuxt-link to="/profile" class="dropdown-item">Profile</nuxt-link>
              <b-dropdown-item href="#" @click.prevent="logout">Sign Out</b-dropdown-item>
            </b-nav-item-dropdown>
            <b-button-group v-else>
              <nuxt-link to="/login" class="mr-2 log-link">Login</nuxt-link>
              <nuxt-link to="/register"class="log-link">Register</nuxt-link>
            </b-button-group>
          </b-navbar-nav>
        </b-collapse>
      </div>

    </b-navbar>
    <b-navbar toggleable="lg" type="light" variant="light">
      <div class="container">
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <nuxt-link to="/" class="nav-link" exact active-class="active">Home</nuxt-link>

          </b-navbar-nav>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">

          </b-navbar-nav>
        </b-collapse>
      </div>

    </b-navbar>
  </div>
</template>

<script>
import {mapGetters} from 'vuex'

export default {
  name: "Navbar",
  data() {
    return {

    }
  },
  computed: {
    ...mapGetters(['isAuthenticated', 'loggedInUser'])
  },
  methods: {
    logout() {
      this.$auth.logout().then(() => {
        this.$router.push({ path: '/' })
      })
    }
  }
}
</script>

<style>
.bg-success {
  background-color:  #00a75e !important;
}
.log-link {
  color: #fff;
  font-size: 17px;
  letter-spacing: 0.6px;
  border: 1px solid #fff;
  padding: 5px 14px;
  border-radius: 7px;
}
.log-link:hover {
  color: #fff;
  text-decoration: none;
}
.navbar-brand {
  font-weight: bold;
  letter-spacing: 1.2px;
  text-transform: uppercase;
}
</style>
