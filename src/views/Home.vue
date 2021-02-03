<template>
  <div>
    <p>{{ dude }}</p>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import {reactive, toRefs, computed } from 'vue'

export default {
  setup() {
    const state = reactive({
      dude: "bulma"
    })

    return {
      ...toRefs(state)
    }

  }
 
};
</script>
 