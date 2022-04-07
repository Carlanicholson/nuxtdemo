<template>
<div class="mx-auto max-w-6xl my-24">
  <form>

    <div class="flex flex-row justify-center">
      <label class="mr-2">Email Address:</label>
      <input class="border border-gray-300" type="email">
    </div>

    <biscuit-choice :options="biscuitOptions" v-model="form.biscuitChoice"/>

  </form>
</div>
</template>

<script>
export default {
  name: "biscuitchoice",
  data(){
    return{
      form: {
        email: null,
        biscuitChoice: null,
      },
      biscuitOptions: [
        {
          name: 'Hobnobs',
          value: 'hobnobs',
        },
        {
          name: 'Malted Milk',
          value: 'malted_milk',
        },
        {
          name: 'Bourbons',
          value: 'bourbons',
        },
        {
          name: 'Shortbread',
          value: 'shortbread',
        }
      ]
    }
  }
  }
</script>
