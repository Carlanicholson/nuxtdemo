<template>
  <div >
    <div class="bg-green-500 text-green-400 flex border rounded-sm border-green-500 ml-12 mr-6">
      <slot name="initial_logo"></slot>
    </div>
    <div class="text-indigo-900 text-4xl">
      <slot name="client_name"></slot>
    </div>
    <div class="text-gray-400 text-sm">
      <slot name="client_email"></slot>
    </div>

    <div class="mr-12">
      <button class="bg-indigo-900 text-white border-indigo-900 rounded-md py-2">
        <slot name="left_button"></slot>
      </button>
      <button class="bg-gray-300 text-indigo-900 border-gray-300 rounded-md py-2">
        <slot name="right_button"></slot>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header"
}
</script>



