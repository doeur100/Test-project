<template>
    <div>
      <h1>Hello about page</h1>
      <p id="timer">{{ timerDisplay }}</p>
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted, onUnmounted } from 'vue';
  
  // Get the element where you want to display the timer
  let timerDisplay = ref('');
  
  // Initialize the timer variables
  let minutes = 4;
  let seconds = 0;
  
  // Function to update the timer display
  function updateTimer() {
    // Decrement the seconds
    seconds--;
  
    // If the seconds reach 0, decrement the minutes and reset the seconds
    if (seconds < 0) {
      minutes--;
      seconds = 59;
    }
  
    // Format the timer display
    const formattedMinutes = minutes.toString().padStart(2, '0');
    const formattedSeconds = seconds.toString().padStart(2, '0');
    const timerText = `${formattedMinutes}:${formattedSeconds}`;
  
    // Update the timer display
    timerDisplay.value = timerText;
  
    // Stop the timer if it reaches 0
    if (minutes === 0 && seconds === 0) {
      clearInterval(timerInterval);
      alert('Time\'s up!');
    }
  }
  
  // Start the timer
  let timerInterval;
  
  onMounted(() => {
    timerInterval = setInterval(updateTimer, 1000);
  });
  
  onUnmounted(() => {
    clearInterval(timerInterval);
  });
  </script>