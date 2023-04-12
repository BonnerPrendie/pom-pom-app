<template>
  <div class="timer">
    <h2>{{ label }}</h2>
    <div class="clock">
      <span>00:00</span>
    </div>
    <ion-button expand="block" shape="round" size="large" @click="startStopTimer">Start Timer</ion-button>
  </div>
</template>

<script setup lang="ts">
  import { IonButton } from '@ionic/vue';

  defineProps({
    label: String,
  });

  let state = false;

  const startStopTimer = () => {
    state = !state; // flip it on or off
    console.log('Inside startStopTimer()', state);

    if (state) {
      // advance the timer
    } else {
      // stop the timer
    }
  };
</script>

<style scoped>
.timer {
  padding: 1rem;
  text-align: center;
  width: 100%;
}

.timer .clock {
  border: 0.5rem solid;
  border-radius: 1rem;
  font-size: 10rem;
  line-height: 10rem;
  margin-bottom: 1rem;
  padding: 1rem 1rem 1.25rem;
  width: 100%;
}

.timer .button {
  height: 6rem;
  font-size: 2.5rem;
}
</style>
