<template>
  <li
    class="my-2 leading-snug bg-white border-b border-gray-400 cursor-pointer rounded bg-gray-100">
    <div class="p-3">
      <p>
        {{ text }}
      </p>
    </div>
  </li>
</template>

<script>
export default {
  props: {
      text: {
          type: String
      }
  },

  setup() {

    return {}
  }
}
</script>
