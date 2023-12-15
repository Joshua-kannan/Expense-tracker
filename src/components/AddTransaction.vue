<template>
    <h3>Add new transaction</h3>
    <form id="form" @submit.prevent="onSubmit">
      <div class="form-control">
        <label for="text">Description</label>
        <input type="text" id="text" placeholder="Enter text..." v-model="text" />
      </div>
      <div class="form-control">
        <label for="amount"
          >Amount <br />
          (For negative use - sign before amount)</label
        >
        <input
          type="text"
          id="amount"
          placeholder="Enter amount..."
          v-model="amount"
        />
      </div>
      <button class="btn">Add transaction</button>
    </form>
  </template>
  
  <script setup>
  import { useToast } from 'vue-toastification';
  import { ref } from 'vue';
  
  const text = ref('');
  const amount = ref('');
  
  // Get toast interface
  const toast = useToast();
  
  const emit = defineEmits(['transactionSubmitted']);
  
  const onSubmit = () => {
    if (!text.value || !amount.value) {
    
      toast.error('Both fields must be filled.');
      return;
    }
  
    const transactionData = {
      text: text.value,
      amount: parseFloat(amount.value),
    };
  
    emit('transactionSubmitted', transactionData);
  
 
    text.value = '';
    amount.value = '';
  };
  </script>