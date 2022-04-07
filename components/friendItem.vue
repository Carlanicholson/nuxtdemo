<template>
  <div class="flex flex-row items-center border rounded-lg border-gray-300 max-w-5xl mx-auto mt-10">
    <div class="w-1/2 p-6 min-h-full">
      <h2 class="text-3xl text-green-600">{{friend.name}}</h2>
      <p class="text-gray-400"> {{ friend.companyName }}</p>
    </div>
    <div class="w-1/4 text-green-400 min-h-full p-6">
      <p>{{friend.age}}</p>
    </div>
    <div class="w-1/4 text-green-400 min-h-full p-6">
      <p>{{ friend.timeUpdated }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "friendItem",
  props: {
    friend: {
      type: Object,
      required: true,
    }
  }
}
</script>
