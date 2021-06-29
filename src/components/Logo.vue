<template>
  <div>
    <a href="#" class="flex item-center py-5 px-2 text-yellow-300 hover:text-yellow-600">
      <ColorSwatchIcon class="h-6 w-6 mr-1" />
      <span class="font-bold">{{ logoText }}</span>
    </a>
  </div>
</template>

<script>
import { ColorSwatchIcon } from "@heroicons/vue/solid";

export default {
  name: "Logo",
  components: { ColorSwatchIcon },
  props: {
    logoText: String,
  },
  data() {
    return {};
  },
};
</script>
