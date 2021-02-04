<template>
  <section
    class="flex-shrink-0 w-max-2xl mb-10 sm:mr-4 p-3 pb-2 bg-gray-200 text-gray-800 rounded-lg shadow-xl">
    <div class="h-full overflow-y-auto">
      <header>
        <h3 class="p-1 font-bold leading-none text-gray-900">{{ title }}</h3>
      </header>

      <ul>
        <Card v-for="card in cards" :text="card.text" :key="card.id"></Card>
      </ul>

      <CardCreateForm/>

    </div>
  </section>
</template>

<script>
/* 
** IMPORTS **
*/
import Card from '@/components/Card.vue'
import CardCreateForm from '@/components/CardCreateForm.vue'

export default {
  components: {
    Card,
    CardCreateForm
  },

  props: {
    title: {
      type: String
    },
    cards: {
      type: Array
    }
  },

  setup() {

    return {}
  }
}
</script>
