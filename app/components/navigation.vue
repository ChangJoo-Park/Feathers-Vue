<template lang="jade">
nav.navbar.navbar-default.navbar-custom.navbar-fixed-top
  .container-fluid
    .navbar-header.page-scroll
      button.navbar-toggle(type='button', data-toggle='collapse', data-target='#headbar-navbar')
        span.sr-only Toggle navigation
        i.fa.fa-bars
      a.navbar-brand(v-link="{path: '/'}") Front-Vue
    #headbar-navbar.collapse.navbar-collapse
      ul.nav.navbar-nav.navbar-right
        li(v-for="route in routes" v-if="!route.meta.excludeMenu")
          router-link(:to="{ name: route.name }") {{route.name}}
</template>

<script>
module.exports = {
  store: ['routes', 'tasks']
}
</script>
