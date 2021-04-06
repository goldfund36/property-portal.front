<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="dark">
      <nuxt-link to="/"><b-navbar-brand>BigPortal</b-navbar-brand></nuxt-link>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <nuxt-link to="/" class="nav-link" exact active-class="active">Home</nuxt-link>

        </b-navbar-nav>

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
            <nuxt-link to="/login" class="mr-2"><b-button variant="warning">Login</b-button></nuxt-link>
            <nuxt-link to="/register"><b-button variant="info">Register</b-button></nuxt-link>
          </b-button-group>
        </b-navbar-nav>
      </b-collapse>
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

<style scoped>

</style>
