<template>
  <div class="max-w-7xl mx-auto">

    <form class="w-1/2 space-y-3 flex flex-col mx-auto mt-24 border rounded-lg p-12 shadow-md" @submit.prevent="addNewWorkflow">
      <label class="text-blue-900 font-boldlight" for="aname">Automation Name:</label>
      <input v-model="form.name" class="border rounded-md p-1 text-sm" type="text" id="aname" name="aname" placeholder="Automation name"><br>
      <label class="text-blue-900 font-boldlight" for="description">Description:</label>
      <input v-model="form.description" class="border rounded-md p-1 text-sm"  type="text" id="description" name="description" placeholder="Description"><br>
      <label class="text-blue-900 font-boldlight" for="totalsteps">Total steps:</label>
      <input v-model="form.totalSteps" class="border rounded-md p-1 text-sm"  type="number" id="totalsteps" name="totalsteps" placeholder="Total steps"><br>
      <div>
        <button type="button" @click="addNewTag">Add additional tag</button>
        <div v-for="tag in form.tags" class="grid grid-cols-2 gap-6">
        <div><label class="text-blue-900 font-boldlight" for="tags">Tags:</label>
          <input v-model="tag.name"  class="border rounded-md p-1 text-sm"  type="text" id="tags" name="tags" placeholder="Tags"><br></div>
        <div> <label class="text-blue-900 font-boldlight" for="class">Class:</label>
          <input v-model="tag.classes" class="border rounded-md p-1 text-sm"  type="text" id="class" name="class" placeholder="Class"><br></div>
      </div>
      </div>
      <button type="submit" class="bg-blue-400 rounded-md border border-blue-900 text-blue-900 font-bold p-3 w-24">Submit</button>
    </form>

    <div class="flex flex-row text-gray-500 text-xs mt-36 mb-6 pl-2">
    <h4 class="w-3/5">WORKFLOW NAME</h4>
    <h4 class="w-1/12">STEPS</h4>
    <h4 class="w-2/6">LAST RUN</h4>
    <h4 class="w-2/6">TAGS</h4>
    </div>
   <automation-item v-for="(workflow, index) in workflows" :key="index" :workflow="workflow"/>

    </div>

</template>

<script>
export default {
  name: 'IndexPage',
  data(){
    return {
      workflows: [
        {
          name: 'Automation name',
          description: 'Short description goes here...',
          totalSteps: 14,
          lastRunAt: new Date(),
          tags: [{
            name: 'New client',
            classes: 'text-blue-500 bg-blue-200'
          },
            {
              name: 'Power user',
              classes: 'text-red-500 bg-red-200'
            }]
        },
        {
          name: 'Automation two',
          description: 'Short description goes here...',
          totalSteps: 14,
          lastRunAt: new Date(),
          tags: [{
            name: 'New client',
            classes: 'text-blue-500 bg-blue-200'
          },
            {
              name: 'Power user',
              classes: 'text-red-500 bg-red-200'
            }]
        },
        {
          name: 'Automation three',
          description: 'Short description goes here...',
          totalSteps: 14,
          lastRunAt: new Date(),
          tags: [{
            name: 'New client',
            classes: 'text-blue-500 bg-blue-200'
          },
            {
              name: 'Power user',
              classes: 'text-red-500 bg-red-200'
            }]
        }
      ],
      form:{
        name: null,
        description: null,
        totalSteps: 0,
        lastRunAt: new Date(),
        tags: [{
          name: null,
          classes: null,
        }]
      }
    }
  },
  methods: {
    addNewTag(){
      this.form.tags.push({
        name: null,
        classes: null
      })
    },
    addNewWorkflow(){
      this.workflows.push(this.form)
      this.form={
        name: null,
        description: null,
        totalSteps: 0,
        lastRunAt: new Date(),
        tags: [{
          name: null,
          classes: null,
        }]
      }
    }
  }
}
</script>
