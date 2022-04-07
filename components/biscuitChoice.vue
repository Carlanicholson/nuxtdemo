<template>
<div>
  <div class="flex  flex-row justify-center">
    <button v-for="option in  options" @click="selectMe(option)" type="button"
            :class="{'bg-green-500': value === option.value}"
    class="bg-green-400 p-6 text-lg text-gray-500 border border-green-500 rounded-md mx-1 my-4"
    >{{ option.name }}</button>
  </div>

</div>
</template>

<script>
export default {
  name: "biscuitChoice",
  props: {
    options:{
      type: Array,
      required: true,
    },
    value: {
      type: String,
      required: true,
    },
  },
  methods: {
    selectMe(option){
      this.$emit('input', option.value);
    }
  }
}
</script>

