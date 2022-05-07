<template>
  <div class="layout">
    <header class="header">
      <Navigation />
    </header>
    <slot/>
  </div>
</template>

<script>

import { BButton } from 'bootstrap-vue';
import Navigation from '~/components/Navigation.vue'
export default {
  components: {
    BButton,
    Navigation
  }
}

</script>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
body {
  font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
  margin:0;
  padding:0;
  line-height: 1.5;
}

.layout {
  max-width: 1000px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.header {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
}

.nav__link {
  margin-left: 20px;
}
</style>
