<template>
    <div>
      <h1>Contador Simple</h1>
      <div class="counter">
        <button id="decrement" @click="decrement">-</button>
        <p>{{ count }}</p>
        <button id="increment" @click="increment">+</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        count: 0
      };
    },
    methods: {
      increment() {
        this.count++;
      },
      decrement() {
        if (this.count > 0) {
          this.count--;
        }
      }
    }
  };
  </script>
  
<style>
    h1 {
        background-color: black;
        color: white;
        border-radius: 50px;
        display: inline;
        padding: 15px;
        margin: 10px;
    }

  .counter {
    display: flex;
    align-items: center;
    text-align: center;
    justify-content: center;

  }
  
  button {
    padding: 10px;
    font-size: 1.5rem;
    margin: 30px;
    border-radius: 50px;
    width: 50px;
    color: white;
    font-weight: 600;
  }

  button:hover {
    transform: scale(1.07);
  }

  #increment{
    background-color: green;
  }

  #decrement{
    background-color: red;
  }
  
  p {
    font-size: 1.5rem;
  }
</style>
  