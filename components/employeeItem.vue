<template>
  <div class="border rounded-lg h-24 mb-4 shadow p-6">
    <div class="flex flex-row items-center text-sm text-blue-400 space-x-12">
      <div class="w-1/4 font-bold text-lg text-blue-500"><h1>{{ employee.name }}</h1></div>
      <div class="w-1/6"><p>{{ employee.age }}</p></div>
      <div class="w-1/5 flex-wrap"><p>{{ employee.address }}</p></div>
      <div class="w-1/5"><p>{{ employee.lastVisited }}</p></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "employeeItem",
  props:{
    employee:{
      type: Object,
      required: true,
    }

  }
}
</script>


