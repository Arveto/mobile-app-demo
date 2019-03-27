<template>
  <div class="root">
    <Message v-for="message in messages" :key="message.id" :message="message"/>
  </div>
</template>

<script>
  import Message from './Message.vue'

  export default {
    name: "Messenger",
    components:{
      Message
    },
    data(){
      return{
        messages: [
          {
            id: 0,
            content: "Hi !",
            from: "Alberto",
            pp: "../assets/logo.png",
            sender: "notme"
          },
          {
            id: 1,
            content: "It is a demo application :)",
            from: "Alberto",
            pp: "../assets/logo.png",
            sender: "notme"
          },
          {
            id: 2,
            content: "Feel free to explore it ! ;)",
            from: "Alberto",
            pp: "../assets/logo.png",
            sender: "notme"
          }
        ]
      }
    }
  }
</script>

<style lang="css" scoped>
  .root{
    text-align: left;
  }
</style>
