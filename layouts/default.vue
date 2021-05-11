<template>
  <div>
<div>
  <b-navbar type="dark" variant="dark">
     <b-navbar-brand href="/">NavBar</b-navbar-brand>
       <b-navbar-nav class="ml-auto">
        <template v-if="$auth.loggedIn">
          <b-nav-item to="/dashboard">Dashboard</b-nav-item>
          <b-nav-item href="#" @click.prevent="logout()">Logout</b-nav-item>
        </template>
        <template v-else>
          <b-nav-item to="/login">Login</b-nav-item>
        </template>
      </b-navbar-nav>
  </b-navbar>
</div>
    <Nuxt />
  </div>
</template>

<script>
export default {
  methods: {
    async logout() {
      try {
        await this.$auth.logout();
      } catch (error) {
        console.log(error);
      }
      this.$router.push('/login')
    }
  }
};
</script>
