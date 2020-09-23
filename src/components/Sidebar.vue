<template>
  <div class="flex flex-col items-center font-noto pt-32 w-64 bg-gray-3">
    <a class="sidebar-link mt-6">Colors</a>
    <a class="sidebar-link mt-6">Typography</a>
    <a class="sidebar-link mt-6">Spaces</a>
    <router-link :to="{ name : 'Buttons'}" class="sidebar-link mt-6">Buttons</router-link>
    <a class="sidebar-link mt-6">Inputs</a>
    <a class="sidebar-link mt-6">Grid</a>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.router-link-exact-active {
  color: #090F31;
}
</style>
