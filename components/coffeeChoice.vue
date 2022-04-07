<template>
  <div>
    <div class="flex flex-row justify-center">
      <button v-for="option in options" @click="selectMe(option)" type="button"
      :class="{'bg-white text-black': value === option.value}"
      class="bg-green-400 p-6 text-lg text-gray-500 border rounded-md">{{ option.name }}</button>
    </div>

    <div class="border rounded-lg bg-green-400 mt-24">
      <slot name="footer">Address</slot>
    </div>
    <div></div>

  </div>

</template>

<script>
export default {
  name: "coffeeChoice",
  props:{
    options:{
    type: Array,
    required: true,
    },
    value: {
      type: String,
      required: true,
    }
  },
  methods:{
    selectMe(option){
      this.$emit('input', option.value)
    }
  }
  }

</script>

