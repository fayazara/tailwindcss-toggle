<template>
  <div class="px-3 py-2 flex items-center justify-between">
    <div class="flex items center space-x-2">
      <div
        class="rounded flex-shrink-0 flex items-center justify-center text-white h-6 w-6"
        :class="options.color"
      >
        <i :class="`fa-xs ${options.icon}`"></i>
      </div>
      <p>{{ options.label }}</p>
    </div>
    <toggle v-model="options.value" />
  </div>
</template>

<script>
export default {
  props: ["options"],
};
</script>