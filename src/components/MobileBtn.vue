<template>
  <div class="md:hidden flex items-center">
    <button @click="mobileMenuToggle($event)">
      <MenuIcon class="h-6 w-6 text-yellow-300" />
    </button>
  </div>
</template>

<script>
import { MenuIcon } from "@heroicons/vue/outline";

export default {
  name: "MobileBtn",
  components: { MenuIcon },
  data() {
    return {
      mobileMenuOpen: false
    }
  },
  methods: {
    mobileMenuToggle(e) {
      this.mobileMenuOpen = !this.mobileMenuOpen;
      this.emitter.emit("toggle-mobile-menu", this.mobileMenuOpen);
    }
  }
};
</script>

<style></style>
