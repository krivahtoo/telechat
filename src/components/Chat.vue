<template>
  <div class="chat">
    <Message v-for="(message, index) in messages" :key="index" :txt="message.txt" :incoming="message.incoming"/>
  </div>
</template>

<script>
import Message from './Message'

export default {
  name: 'Chat',
  components: {
    Message
  },
  data () {
    return {
      messages: [
        {
          txt: 'Hey, man! What\'s up, Mr Stark? 👋',
          incoming: true
        },
        {
          txt: 'Kid, where\'d you come from?',
          incoming: false
        },
        {
          txt: 'Field trip! 🤣',
          incoming: true
        },
        {
          txt: 'Uh, what is this guy\'s problem, Mr. Stark? 🤔',
          incoming: true
        },
        {
          txt: 'Uh, he\'s from space, he came here to steal a necklace from a wizard.',
          incoming: false
        },
        {
          txt: 'Hey, man! What\'s up, Mr Stark? 👋',
          incoming: true
        },
        {
          txt: 'Kid, where\'d you come from?',
          incoming: false
        },
        {
          txt: 'Field trip! 🤣',
          incoming: true
        },
        {
          txt: 'Uh, what is this guy\'s problem, Mr. Stark? 🤔',
          incoming: true
        },
        {
          txt: 'Uh, he\'s from space, he came here to steal a necklace from a wizard.',
          incoming: false
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.chat {
  display: flex;
  height: 100%;
  flex-direction: column;
  justify-content: flex-start;
  background-color: rgb(243, 243, 243);
  flex-shrink: 2;
  overflow-y: auto;

  box-shadow:
    inset 0 2rem 2rem -2rem rgba(black, 0.05),
    inset 0 -2rem 2rem -2rem rgba(black, 0.05);
}
</style>
