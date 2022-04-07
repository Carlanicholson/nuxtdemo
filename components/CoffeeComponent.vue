<template>
  <div class=" max-w-4xl mx-auto flex items-center justify-center">
    <button v-for="item in items" @click="selectMe(item)" type="button"
            class="border rounded-md p-4"
             :class="{'bg-green-300': value === item.value, 'bg-green-500': value !== item.value}"

    >{{item.name}} - £{{item.price}}</button>
  </div>
</template>

<script>
export default {
  name: "CoffeeComponent",
  props: {
    items: Object,
    value:{
      type: String,
      required: true,
    },
  },

methods:{
    selectMe(item){
      this.$emit('input', item.value)
    }
}
}
</script>

