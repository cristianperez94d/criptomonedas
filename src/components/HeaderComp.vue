<template>
  <header class="shadow w-screen">
    <nav>
      <nav
        class="flex items-center justify-between flex-wrap bg-yellow-400 p-6"
      >
        <div class="flex items-center flex-shrink-0 text-white mr-6">
          <IconComp class="mr-2" />
          <router-link :to="{ name: 'Home' }" class="font-semibold text-xl tracking-tight"
            >Cryptomonedas</router-link
          >
        </div>
        <div
          class="hidden sm:block w-full block flex-grow lg:flex lg:items-center lg:w-auto"
        >
          <div class="text-sm lg:flex-grow"></div>
        </div>
      </nav>
    </nav>
  </header>
</template>
<script>
import IconComp from '@/components/IconComp';
export default {
  name: 'HeaderComp',
  components: { IconComp },
};
</script>
