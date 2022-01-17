<template>
  <nav class="flex items-center justify-between flex-wrap p-6 header">
    <div class="flex items-center flex-no-shrink text-white mr-6">
        <span class="font-semibold text-left text-xl tracking-tight">
            Football Player<br/>Profile App
        </span>
    </div>
    <div class="block lg:hidden">
      <button
        class="
          flex
          items-center
          px-3
          py-2
          border
          rounded
          text-teal-lighter
          border-teal-light
          hover:text-white hover:border-white
        "
      >
        <svg
          class="h-3 w-3"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <title>Menu</title>
          <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"></path>
        </svg>
      </button>
    </div>
    <div class="w-full block flex-grow lg:flex lg:items-center lg:w-auto">
      <div class="text-sm lg:flex-grow">
      </div>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
    .header {
        background: #040409;
    }
</style>
