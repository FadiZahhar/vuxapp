<template>
  <div>
  <TheHeader @sidenavToggle="displaySidenav = !displaySidenav" />
  <TheSidenav 
  :show="displaySidenav"
  @close="displaySidenav = false"
  />
    <nuxt/>
  </div>
</template>

<script>
import TheHeader from '@/components/Navigation/TheHeader'
import TheSidenav from '@/components/Navigation/TheSidenav'
export default {
  components: {
    TheHeader,
    TheSidenav
  },
  data() {
    return {
      displaySidenav: false
    }
  }
}
</script>

<style>
html {
font-family: 'Open Sans';
  font-style: normal;
  font-size: 16px;
}

body {
  margin:0;
}

</style>
