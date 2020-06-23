<template>
  <div class="container">
    <div>
      <Logo />
      <Socials />
    </div>
  </div>
</template>

<script>
import Socials from "~/components/Socials.vue";

export default {
  components: {
    Socials,
  },
}
</script>

<style>
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}
</style>
