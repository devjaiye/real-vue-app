<script setup>
  import EventCard from '@/components/EventCard.vue'; //..@ makes it absolute path
  import {onMounted, ref} from 'vue'
import EventService from '@/services/EventService';

const events = ref(null)

onMounted(()=> {
  EventService.getEvents()
  .then((res)=>{
   events.value = res.data
  })
  .catch((error) =>{
    console.log(error)
  })
})

</script>

<template>
  <h1>Events For You</h1>
<div class="events">
  <EventCard v-for="event in events" :event="event" :key="event.id"/>
</div>
</template>

<style scoped>
  .events{
    display: flex; 
    flex-direction: column;
    align-items: center;
    
  }

</style>
