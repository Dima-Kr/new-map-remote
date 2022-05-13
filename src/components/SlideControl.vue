<script setup>

  import {onMounted, ref} from 'vue'
  import * as Ably from 'ably'
  import ImageButtons from './ImageButtons.vue';
  const client = new Ably.Realtime(import.meta.env.VITE_ABLY_API)
  const channel = client.channels.get('carousel')

  // array of buttons to be populated in the template, with the name of the button and the id that will be set via ably
  const buttonName = [
    {id: 'img-01', name: 'Image 1'},
    {id: 'img-02', name: 'Image 2'},
    {id: 'img-03', name: 'Image 3'},
    {id: 'img-04', name: 'Image 4'},
    {id: 'img-05', name: 'Image 5'},
    {id: 'img-06', name: 'Image 6'},
    {id: 'img-07', name: 'Image 7'},
    {id: 'img-08', name: 'Image 8'},
    {id: 'img-09', name: 'Image 9'},
    {id: 'img-10', name: 'Image 10'},
  ]
  
  onMounted(() => {
    client.connection.on('connected',function(){
      console.log('connected to ably')
    })
  })
  
  // function to publish the image id via ably message
  function selectImage(id){
    channel.publish('image selected', id)
  }

</script>

<template>

<ImageButtons 
v-for="button in buttonName"
:key="button"
:title="button.name"
:id="button.id"
@click="selectImage(button.id)"
/>

</template>

<style>

</style>