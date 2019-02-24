<template>
  <header class="header">
    <logo/>
  </header>
</template>

<script>
import Logo from "~/components/Logo.vue";

export default {
  components: {
    Logo
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Staatliches");
.header {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  width: 100%;
  height: 100vh;
  background-image: linear-gradient(to top, #5f72bd 0%, #9b23ea 100%);
}
</style>
