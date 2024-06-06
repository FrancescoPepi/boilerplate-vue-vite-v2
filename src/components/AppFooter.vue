<script>
import AppFooterSC from "./subComponentsFooter/AppFooterSC.vue";

export default {
  data() {
    return {
      title: "FOOTER",
    };
  },

  components: {
    AppFooterSC,
  },
};
</script>

<template>
  <h1>{{ title }}</h1>
  <AppFooterSC />
</template>

<style lang="scss" scoped></style>
