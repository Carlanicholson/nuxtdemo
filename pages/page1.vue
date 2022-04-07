<template>
<div class="max-w-7xl mx-auto">

  <form class="space-y-2 mt-24" @submit.prevent="addNewPerson">
    <label for="name">Name:</label>
    <input v-model="form.name" type="text" id="name" name="name" placeholder="Full Name" class="ml-4 border rounded-md p-1"><br>
    <label for="age">Age:</label>
    <input v-model="form.age" type="number" id="age" name="age" placeholder="Age" class="ml-4 border rounded-md p-1"><br>
    <label for="address">Address:</label>
    <input v-model="form.address" type="text" id="address" name="address" placeholder="Full Address" class="ml-4 border rounded-md p-1"><br>
    <button type="submit" class="border rounded-full p-2 bg-gray-200">Submit</button>
  </form>


  <div class="flex flex-row text-gray-400 mt-24 p-4 space-x-12">
  <h4 class="w-1/4">Name</h4>
  <h4 class="w-1/6">Age</h4>
  <h4 class="w-1/4">Address</h4>
  <h4 class="w-2/6">Last visited</h4>
  </div>
<employee-item v-for="(employee,index) in employees" :key="index" :employee="employee"></employee-item>

</div>
</template>


<script>
export default {
  name: "page1",
  data: function () {
    return {
      employees: [
        {
          name: 'Carla Nicholson',
          age: 27,
          address: '1234 flower gardens, hedge end,  southampton, SO50 6PP',
          lastVisited: new Date(),
        },

        {
          name: 'Willow Nicholson',
          age: 1,
          address: '1234 flower gardens, hedge end,  southampton, SO50 6PP',
          lastVisited: new Date(),
        },

        {
          name: 'Matt Nicholson',
          age: 35,
          address: '1234 flower gardens, hedge end,  southampton, SO50 6PP',
          lastVisited: new Date(),
        }
      ],

    form: {
      name: null,
        age: 0,
        address: null,
      lastVisited: new Date(),
    }
    }
  },

  methods:{
    addNewPerson(){
      this.employees.push(this.form)
      this.form={
        name: null,
        age: 0,
        address: null,
        lastVisited: new Date(),
      }
    }
  }
}


</script>
