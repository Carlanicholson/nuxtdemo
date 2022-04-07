<template>
    <div>
      <form class="flex flex-col items-center mt-12" @submit.prevent="addNewFriend">
        <label for="name">Name:</label>
        <input v-model="form.name" class="border rounded-sm" type="text" id="name" name="name">
        <label for="company">Company Name:</label>
        <input v-model="form.companyName" class="border rounded-sm" type="text" id="company" name="company">
        <label for="age">Age:</label>
        <input v-model="form.age" class="border rounded-sm" type="text" id="age" name="age">
        <button class="border rounded-md bg-yellow-400 p-2 mt-6" type="submit">Submit</button>
      </form>

      <friend-item v-for="(friend, index) in  friends" :key="index" :friend="friend"/>

      <div>
        <h1>Hello World!</h1>
      </div>
    </div>
</template>

<script>
export default {
  name: "page2",
  data(){
    return {
      friends: [
        {
        name: 'Carla Nicholson',
        companyName: 'Codepotato',
        age: 27,
        timeUpdated: new Date()
    },
      {
        name: 'Matthew Nicholson',
        companyName: 'Whites',
        age: 35,
        timeUpdated: new Date()
      },
        {
          name: 'Willow Nicholson',
          companyName: 'N/A',
          age: 1,
          timeUpdated: new Date()
        }
      ],
      form: {
        name: null,
        companyName: null,
        age: 0,
        timeUpdated: new Date()
    }
    }
  },
  methods: {
    addNewFriend(){
      this.friends.push(this.form)
      this.form={
        name: null,
        companyName: null,
        age: 0,
        timeUpdated: new Date()
      }
    }
  }
}
</script>
