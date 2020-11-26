<template>
  <div id="telechat">
    <div class="main">
      <div class="header"></div>
      <Chat/>
      <div class="footer"></div>
    </div>
  </div>
</template>

<script>
import Chat from './components/Chat'

export default {
  name: 'App',
  components: {
    Chat
  }
}
</script>

<style lang="scss">
#telechat {
  z-index: 9999;
  .main {
    position: absolute;
    bottom: 5%;
    right: 5%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background-color: rgb(232, 232, 232);
    width: 350px;
    height: 550px;
    border-radius: 30px 30px 0 30px;
    box-shadow: 0 0 2rem 0 rgba(black, 0.4);
    &>.header {
      width: 100%;
      height: 60px;
      background-color: rgba(11, 11, 40, 1);
      border-radius: 30px 30px 0 0;
    }
    &>.footer {
      width: 100%;
      height: 60px;
      background-color: rgba(11, 11, 40, 1);
      border-radius: 0 0 0 30px;
    }
  }
}
@keyframes typing {
  0%, 75%, 100% {
    transform: translate(0, 0.25rem) scale(0.9);
    opacity: 0.5;
  }

  25% {
    transform: translate(0, -0.25rem) scale(1);
    opacity: 1;
  }
}
</style>
