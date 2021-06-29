<template>
  <nav class="bg-gray-800">
    <div class="max-w-5xl xl:max-w-full mx-auto px-8">
      <div class="flex justify-between">
        <!-- Primary Nav -->
        <PrimaryNav />
        <!-- logo -->
        <Logo logoText="SCUBA DIVING" />
        <!-- Secondary Nav -->
        <SecondaryNav />
        <!-- Mobile Button -->
        <MobileBtn />
      </div>
    </div>
    <!-- Mobile menu -->
    <MobileMenu />
  </nav>
</template>

<style scoped></style>

<script setup>
import Logo from "./Logo.vue";
import PrimaryNav from "./PrimaryNav.vue";
import SecondaryNav from "./SecondaryNav.vue";
import MobileBtn from "./MobileBtn.vue";
import MobileMenu from "./MobileMenu.vue";

</script>
