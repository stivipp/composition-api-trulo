<template>
    <form action="">
                <textarea class="w-full border-t border-l border-gray-300 p-3 outline-none rounded shadow-inner" rows="3"></textarea>

                <div class="flex mt-1 items-center">
                  <button class="py-1 px-3 font-semibold text-gray-50 rounded border-b border-gray-600 text-shadow outline-none
                                 bg-green-500 hover:bg-green-400 active:bg-green-400 focus:outline-none">
                       Add card
                  </button>
                

                <a class="ml-0.5 p-1 text-gray-500 hover:text-gray-700" href="#">
                  <svg class="w-6 h-6 fill-current" viewBox="0 0 20 20">
                    <path d="M10.185,1.417c-4.741,0-8.583,3.842-8.583,8.583c0,4.74,3.842,8.582,8.583,8.582S18.768,14.74,18.768,10C18.768,5.259,14.926,1.417,10.185,1.417 M10.185,17.68c-4.235,0-7.679-3.445-7.679-7.68c0-4.235,3.444-7.679,7.679-7.679S17.864,5.765,17.864,10C17.864,14.234,14.42,17.68,10.185,17.68 M10.824,10l2.842-2.844c0.178-0.176,0.178-0.46,0-0.637c-0.177-0.178-0.461-0.178-0.637,0l-2.844,2.841L7.341,6.52c-0.176-0.178-0.46-0.178-0.637,0c-0.178,0.176-0.178,0.461,0,0.637L9.546,10l-2.841,2.844c-0.178,0.176-0.178,0.461,0,0.637c0.178,0.178,0.459,0.178,0.637,0l2.844-2.841l2.844,2.841c0.178,0.178,0.459,0.178,0.637,0c0.178-0.176,0.178-0.461,0-0.637L10.824,10z"></path>
                  </svg>
                </a>
              
              </div>
            </form>
</template>

<script>
import { reactive, toRefs } from 'vue'

export default {
    setup () {
        const state = reactive({
            count: 0,
        })
    
        return {
            ...toRefs(state),
        }
    }
}
</script>
