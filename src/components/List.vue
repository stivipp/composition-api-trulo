<template>
  <section
    class="flex-shrink-0 w-full mb-10 p-3 pb-2 bg-gray-200 text-gray-800 rounded-lg shadow-xl"
  >
    <div class="h-full overflow-y-auto">
      <header>
        <h3 class="p-1 font-bold leading-none text-gray-900">{{ title }}</h3>
      </header>

      <ul>
        <Card></Card>
      </ul>
    </div>
  </section>
</template>

<script>
import { reactive, toRefs } from 'vue'
import Card from '@/components/Card.vue'

export default {
  components: {
    Card
  },

  props: {
    title: {
      type: String
    }
  },

  setup() {
    const state = reactive({
      count: 0
    })

    return {
      ...toRefs(state)
    }
  }
}
</script>
