<template>
  <div>
    <SideBar />
    <NavBar />
    <Nuxt />
  </div>
</template>


<script>
import SideBar from '~/components/side-bar.vue';
import NavBar from '~/components/navbar.vue';

export default {
  components: { SideBar, NavBar },
}
</script>
