<template>
  <main class="flex h-screen bg-purple-500 lg:bg-gradient-to-r from-red-500 to-pink-400">
    <div class="sm:flex items-start w-screen px-4 py-10 overflow-x-auto">

      <List v-for="list in lists"
       :title="list.title"
       :cards="list.cards" 
       :key="list.id"
      />

      <ListCreateForm @new-list-coming="addNewList($event)"/>

    </div>
  </main>
</template>

<script>
import { ref, onMounted } from 'vue'
import { data } from '@/data.js'

import List from '@/components/List.vue'
import ListCreateForm from '@/components/ListCreateForm.vue'


export default {
  components: {
    List,
    ListCreateForm
  },

  setup() {
    const lists = ref(data)

    const addNewList = title => {
      lists.value.push({
        id: Math.max(...lists.value.map(list => list.id)) + 1 ,
        title: title,
        cards: []
      })
      
    }

    //events
    onMounted( () => {
      window.eventBus.on('new-card-coming', event => console.log(event))
    })


    return { 
      lists,
      addNewList
      }
  }
}
</script>
