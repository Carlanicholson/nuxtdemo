<template>
 <div>
   <div class="flex justify-center ">
   <label for="email">Email:</label>
   <input type="email" id="email" name="email" placeholder="email">
   </div>
   <coffee-component :items="plans" v-model="form.CoffeeComponent"></coffee-component>

 </div>
</template>

<script>
export default {
  name: "Coffeeplan",
  data(){
    return {
      form:{
        email: null,
        CoffeeComponent: null,
      },
      plans: [
        {
          name: 'Latte',
          price: 7,
          value: 'latte'
        },
        {
          name: 'Flat White',
          price: 4,
          value: 'flat_white'
        },
        {
          name: 'Espresso',
          price: 2,
          value: 'espresso'
        }]
    }
  }
}

</script>

