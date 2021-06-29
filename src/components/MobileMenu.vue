<template>
  <div
    :class="{ open: !isOpen }"
    class="mobile-nav flex flex-col items-center py-2 pb-4 text-sm bg-gray-800"
  >
    <a href="#" :class="{ fade: isOpen }" class="py-3 px-3 text-yellow-500">Features</a>
    <a href="#" :class="{ fade: isOpen }" class="py-3 px-3 text-yellow-500">Pricing</a>
    <a href="#" :class="{ fade: isOpen }" class="py-3 px-3 text-yellow-500">Login</a>
    <a href="#" :class="{ fade: isOpen }" class="py-2 px-3 bg-pink-900 text-white rounded">Register</a>
  </div>
</template>

<script>
export default {
  name: "MobileMenu",
  data() {
    return {
      isOpen: false,
    };
  },
  mounted() {
    this.emitter.on("toggle-mobile-menu", (isOpen) => {
      this.isOpen = isOpen;
    });
  },
};
</script>

<style scoped>
.mobile-nav {
  position: fixed;
  height: 100vh;
  width: 100%;
  clip-path: circle(900px at 90% -38%);
  -webkit-clip-path: circle(900px at 90% -38%);
  transition: all 1s ease-in-out;
  pointer-events: none;
}

.mobile-nav.open {
  clip-path: circle(100px at 90% -38%);
  -webkit-clip-path: circle(100px at 90% -38%);
  pointer-events: all;
}

a {
  opacity: 0;
}

a:nth-child(1) {
  transition: all 0.3s ease 0.2s;
}

a:nth-child(2) {
  transition: all 0.3s ease 0.4s;
}

a:nth-child(3) {
  transition: all 0.3s ease 0.6s;
}

a:nth-child(4) {
  transition: all 0.3s ease 0.8s;
}

a.fade {
  opacity: 1;
}
</style>
