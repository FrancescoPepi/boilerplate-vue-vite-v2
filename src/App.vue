<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";
import AppUpViewport from "./components/AppUpViewport.vue";

export default {
  data() {
    return {
      scTimer: 0,
      scY: 0,
    };
  },

  components: {
    AppHeader,
    AppMain,
    AppFooter,
    AppUpViewport,
  },
};
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
  <AppUpViewport />
</template>

<style lang="scss"></style>
