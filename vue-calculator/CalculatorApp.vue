<template>
    <div class="flex flex-col items-center justify-center min-h-screen bg-gray-100">
      <h1 class="text-2xl font-bold mb-4">Calculadora</h1>
      <div class="grid grid-cols-3 gap-2">
        <button 
          v-for="num in numbers" 
          :key="num" 
          @click="selectNumber(num)" 
          class="p-4 text-xl font-bold bg-white border rounded-lg shadow hover:bg-gray-200">
          {{ num }}
        </button>
      </div>
      <p v-if="selectedNumber !== null" class="mt-4 text-lg">
        Has clicat el nombre: <strong>{{ selectedNumber }}</strong>
      </p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        numbers: [1, 2, 3, 4, 5, 6, 7, 8, 9],
        selectedNumber: null,
      };
    },
    methods: {
      selectNumber(num) {
        this.selectedNumber = num;
      },
    },
  };
  </script>
  
  <style>
  body {
    font-family: Arial, sans-serif;
  }
  </style>
  