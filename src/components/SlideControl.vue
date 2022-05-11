<script setup>

  import {onMounted} from 'vue'
  import * as Ably from 'ably'
  const client = new Ably.Realtime(import.meta.env.VITE_ABLY_API)
  const channel = client.channels.get('carousel')
  
  onMounted(() => {
    client.connection.on('connected',function(){
      console.log('connected to ably')
    })
  })

  function Img01(){
    channel.publish('img-01', 'load img 1')
  }
  function Img02(){
    channel.publish('img-02', 'load img 2')
  }
  function Img03(){
    channel.publish('img-03', 'load img 3')
  }
  function Img04(){
    channel.publish('img-04', 'load img 4')
  }
  function Img05(){
    channel.publish('img-05', 'load img 5')
  }
  function Img06(){
    channel.publish('img-06', 'load img 6')
  }
  function Img07(){
    channel.publish('img-07', 'load img 7')
  }
  function Img08(){
    channel.publish('img-08', 'load img 8')
  }
  function Img09(){
    channel.publish('img-09', 'load img 9')
  }
  function Img10(){
    channel.publish('img-10', 'load img 10')
  }

</script>

<template>
  <button @click="Img01" class="Img01">Image 1</button>
  <button @click="Img02" class="Img02">Image 2</button>
  <button @click="Img03" class="Img03">Image 3</button>
  <button @click="Img04" class="Img04">Image 4</button>
  <button @click="Img05" class="Img05">Image 5</button>
  <button @click="Img06" class="Img06">Image 6</button>
  <button @click="Img07" class="Img07">Image 7</button>
  <button @click="Img08" class="Img08">Image 8</button>
  <button @click="Img09" class="Img09">Image 9</button>
  <button @click="Img10" class="Img20">Image 10</button>
</template>

<style>

</style>