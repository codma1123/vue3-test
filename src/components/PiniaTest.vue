<template>
  <div>
    counter : {{ counter }} 
  </div>
  <div>
    <button @click="increaseCounter">
      click!
    </button>
  </div>
</template>

<script>
import { useCounterStore } from '@/stores/counter'

export default {
  setup() {
    const counterStore = useCounterStore()

    return { counterStore }
  },
  computed: {
    
  },
  methods: {
    increaseCounter() {
      console.log('ss')
      this.counterStore.increment()
      console.log('new count:', this.counterStore.count)
    }
  }
}
</script>