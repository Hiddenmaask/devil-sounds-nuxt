<template>
  <div class="text-black dark:text-white">
    <div></div>

    <slot />

    <div class="grid grid-cols-2 content-between px-4">
      <NuxtLink to="/index">
        Home
      </NuxtLink>
      <NuxtLink to="/about" class="text-right">
        About
      </NuxtLink>
    </div>

  </div>
</template>

<script>
export default {
  name: "custom"
}
</script>

<style scoped>

</style>


