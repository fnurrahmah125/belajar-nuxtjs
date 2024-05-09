<template>
  <header class="w-full border-b border-slate-200 py-6">
    <div class="container mx-auto">
      <div class="flex flex-col md:flex-row justify-between items-center px-4">
        <div class="mb-4 md:mb-0">
          <NuxtLink to="/" class="text-2xl text-orange-600 font-bold"
            >Toko Online</NuxtLink
          >
        </div>
        <nav class="flex items-center gap-6">
          <NuxtLink to="/" class="text-base hover:text-orange-600"
            >Home</NuxtLink
          >
          <NuxtLink to="/product" class="text-base hover:text-orange-600"
            >Products</NuxtLink
          >
          <NuxtLink to="/cart" class="text-base hover:text-orange-600"
            >Cart</NuxtLink
          >
        </nav>
      </div>
    </div>
  </header>
</template>
