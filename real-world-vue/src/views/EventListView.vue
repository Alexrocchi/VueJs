<script setup>
import EventServide from '@/services/EventService.js';
import EventCard from '@/components/EventCard.vue';
import {ref, onMounted} from 'vue';

const events = ref(null);

onMounted(() => {
  EventServide.getEvents()
  .then((response) => {
    events.value = response.data;
  })
  .catch((error) => {
    console.log(error);
  })
})

</script>

<template>
  <main>
    <h1>Events For Good</h1>
    <div class="events">
      <EventCard v-for="event in events" :key="event.id" :event="event"/>
    </div>
  </main>
</template>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>