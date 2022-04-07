<template>
  <div>
    <div class="flex flex-row min-w-full space-between">
    <div class=" flex flex-row items-center ml-12 mt-8 mr-auto">
      <button class="text-indigo-900">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" viewBox="0 0 20 20" fill="currentColor">
          <path
            d="M10.707 2.293a1 1 0 00-1.414 0l-7 7a1 1 0 001.414 1.414L4 10.414V17a1 1 0 001 1h2a1 1 0 001-1v-2a1 1 0 011-1h2a1 1 0 011 1v2a1 1 0 001 1h2a1 1 0 001-1v-6.586l.293.293a1 1 0 001.414-1.414l-7-7z"/>
        </svg>
      </button>
      <h4 class="text-gray-400">Home /</h4>
      <h4 class="text-gray-400"> Clients /</h4>
    </div>

      <div class=" flex items-center mt-8 mr-12">
        <button class="border rounded-md p-2 mx-2">Updates</button>
        <button class="bg-pink-500 rounded-full w-8 px-2 mx-2 text-white">1</button>
        <button>
          <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-6 mx-2 " fill="none" viewBox="0 0 24 24" stroke="currentColor"
               stroke-width="1">
            <path stroke-linecap="round" stroke-linejoin="round"
                  d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"/>
          </svg>
        </button>
        <input class="border rounded-md p-2 mx-2 " type="text" placeholder="Search...">
      </div>
    </div>
    <div class="mt-4 mb-12">
      <hr>
    </div>

    <div class="flex flex-row min-w-full space-between">

      <Header-Component>
        <template #initial_logo>DA</template>
      </Header-Component>

      <div class="mr-auto">
        <Header-Component>
          <template #client_name>Daisy Adams</template>
          <template #client_email>daisyadams@yahoo.co.uk</template>
        </Header-Component>

      </div>
        <header-component>
          <template #left_button>Add New</template>
          <template #right_button>Action</template>
        </header-component>

    </div>

    <div class="ml-12">
      <input class=" border rounded-md" type="text" v-model="value">
      <input class=" border rounded-md" type="text" v-model="lastname">
      <p>Value: {{ value }}</p>
      <p>Name: {{ lastname }}</p>
    </div>

  </div>
</template>

<script>
export default {
  name: "header",
  data(){
    return{
      value: null,
      lastname: null,
    }
  }
}
</script>
