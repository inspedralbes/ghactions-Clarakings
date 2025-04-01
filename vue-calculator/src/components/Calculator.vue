<template>
    <div>
      <div class="calculator">
        <button v-for="number in numbers" :key="number" @click="handleClick(number)">
          {{ number }}
        </button>
      </div>
      <div v-if="clickedNumber">
        Has clicat al número: {{ clickedNumber }}
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        numbers: [1, 2, 3, 4, 5, 6, 7, 8, 9],
        clickedNumber: null,
      };
    },
    methods: {
      handleClick(number) {
        this.clickedNumber = number;
      },
    },
  };
  </script>
  
  <style scoped>
  .calculator {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
  }
  button {
    padding: 20px;
    font-size: 1.5em;
    cursor: pointer;
  }
  </style>
  