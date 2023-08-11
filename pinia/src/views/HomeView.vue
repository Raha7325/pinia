<template>
  <div class="home">
    <div class="counter">
      {{ storeCounter.count }}
    </div>
    <div class="buttons">
      <button @click="storeCounter.decreaseCount">-</button>
      <button @click="storeCounter.increaseCount">+</button>
    </div>
    <hr />
    <div>
      this counter is : {{ storeCounter.oddOrEven }}
    </div>
  </div>
   
</template>

<script setup>
  import { useCounterStore } from '@/stores/counter'

const storeCounter = useCounterStore()

</script>
<style>
.counter {
  font-size: 60px;
  margin: 20px;
}
.buttons button {
  font-size: 40px;
  margin: 10px;
}
</style>