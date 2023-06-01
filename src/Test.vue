<template>
  <div id="foo">
  <span>{{state.count}}</span>  
    <div id="app2">
      <button @click="count++, state.count++">Count is: {{ count }}</button>
      <div>oi</div>
      <div>oi</div>
      <button @click="increment">
        {{ state.count }}
      </button>
      <span>{{state.count}}</span>  
    </id>
  </id>
</template>

<script>
import { reactive } from 'vue'

export default {
  setup() {
    const state = reactive({count: 0});

    function increment() {
      state.count++
    }

    // expose the state to the template
    return { 
      state, 
      increment
    }
  },
  data() {
    return {
      count: 0,
    };
  },
};
</script>

<style scoped>
button {
  font-weight: bold;
}

#app {
  width: 100px;
  height: 200px;

  background-color: red;

  display: flex;
  flex-flow: column nowrap;  
}
</style>
