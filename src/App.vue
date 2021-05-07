<template>
  <main>
    <header-comp />
    <router-view class="container px-5 sm:px-20 py-20 flex justify-center" />
  </main>
</template>

<script>
import HeaderComp from '@/components/HeaderComp';
export default {
  name: 'App',
  components: { HeaderComp },
};
</script>
