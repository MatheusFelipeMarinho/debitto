<template>
  <div>
    <top-nav-bar />
    <!-- <hr /> -->
    <sub-nav-bar />
  </div>
</template>

<script>
import TopNavBar from "./app/TopNavBar.vue";
import SubNavBar from "./app/SubNavBar.vue";
export default {
  components: { TopNavBar, SubNavBar },
};
</script>

<style>
</style>