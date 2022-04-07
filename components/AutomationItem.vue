<template>
  <div class="border rounded-md h-24 p-6 shadow-sm mb-4">
    <div class="flex flex-row items-center pl-2">
      <div class="w-3/5">
        <h1 class="text-blue-900 text-lg font-bold">{{workflow.name}}</h1>
        <p class="text-gray-500 text-xs font-light">{{workflow.description}}</p>
      </div>

      <div class="w-1/12">
        <p class="text-gray-500 text-sm font-light">{{workflow.totalSteps}}</p>
      </div>

      <div class="w-2/6">
        <p class="text-gray-500 text-sm font-light flex flex-row"><svg class="w-7 pr-2" xmlns="http://www.w3.org/2000/svg" className="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" strokeWidth={2}>
          <path strokeLinecap="round" strokeLinejoin="round" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
        </svg>
          {{workflow.lastRunAt}}</p>
      </div>
      <div class="w-2/6">
        <div class=" flex flex-row pl-2 space-x-2">
          <p v-for="tag in workflow.tags" :class="tag.classes" class="text-xs p-1 inline-flex rounded">{{tag.name}}</p>
          <p class="text-blue-500 pl-14"><svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
            <path stroke-linecap="round" stroke-linejoin="round" d="M9 5l7 7-7 7" />
          </svg></p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Automation item",
  props:{
    workflow: {
      type: Object,
      required: true
    }
  }
}
</script>

