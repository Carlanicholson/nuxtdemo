<template>
  <div class="mx-auto max-w-6xl my-24">
    <form>

      <div class="flex flex-row justify-center">
        <label class="mr-2">Email Address:</label>
        <input class="border border-gray-300" type="email">
      </div>

      <coffee-choice :options="coffeeOptions" v-model="form.coffeeChoice"/>

    </form>

<coffee-choice><template #footer> Address 2</template></coffee-choice>
  <div><button @click="count++"> Count is {{count}}</button> </div>

  </div>
</template>


<script>
export default {
  name: "coffee",
  data() {
    return {
      count: 0,

      form: {
        email: null,
        coffeeChoice: null,
      },
      coffeeOptions: [
        {
          name: 'latte',
          value: 'latte'
        },
        {
          name: 'flat white',
          value: 'flat_white'
        },
        {
          name: 'cappuccino',
          value: 'cappuccino'
        }
      ]

    }
  }
}
</script>


