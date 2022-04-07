<template>
<div>
  <header class="justify-between flex items-center mt-6 border-b-2 border-dashed ">
    <h1 class="text-2xl">Dad Jokes</h1>
    <ul class=" flex text-gray-400">
      <li class="bg-blue-300 p-3 mx-1 mb-2">
      <nuxt-link to="/">Home</nuxt-link>
    </li>
      <li class="bg-blue-300 p-3 mx-1 mb-2">
      <nuxt-link to="/jokes">Jokes</nuxt-link>
    </li>
      <li class="bg-blue-300 p-3 mx-1 mb-2">
      <nuxt-link to="/about">About</nuxt-link>
    </li>
    </ul>
  </header>
</div>
</template>

<script>
export default {
  name: "AppHeader"
}
</script>
