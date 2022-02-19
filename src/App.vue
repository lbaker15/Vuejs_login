<template>
  <AppHeader/>
  <router-view/>
</template>

<style lang="scss">
</style>

<script>
  import AppHeader from '@/components/AppHeader.vue';

  export default {
    components: {
      AppHeader
    } 
  }
</script>
