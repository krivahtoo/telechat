<template>
  <div id="telechat">
    <div v-if="open" class="main">
      <div class="header">
        <span class="icon">
          <CloseIcon />
        </span>
      </div>
      <Chat/>
      <div class="footer">
        <input type="text" placeholder="Type your message here!">
        <button>
          <SendIcon />
        </button>
      </div>
    </div>
    <div v-else class="icon">
      <div class="typing typing-1"></div>
      <div class="typing typing-2"></div>
      <div class="typing typing-3"></div>
    </div>
  </div>
</template>

<script>
import Chat from './components/Chat'
import SendIcon from 'vue-material-design-icons/Send'
import CloseIcon from 'vue-material-design-icons/Close'

export default {
  name: 'App',
  data: () => {
    return {
      open: true
    }
  },
  components: {
    Chat,
    SendIcon,
    CloseIcon
  }
}
</script>

<style lang="scss">
#telechat {
  z-index: 9999;
  position: absolute;
  bottom: 5%;
  right: 5%;
  .main {
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background-color: rgb(232, 232, 232);
    width: 350px;
    height: 550px;
    border-radius: 30px 30px 0 30px;
    box-shadow: 0 0 2rem 0 rgba(black, 0.4);
    &>.header {
      flex-basis: 3.5rem;
      flex-shrink: 0;
      margin-bottom: 0.5rem;
      box-sizing: border-box;
      background-color: rgba(11, 11, 40, 1);
      border-radius: 30px 30px 0 0;

      > .icon {
        position: relative;
        margin-right: auto;
        top: 8px;
        left: 315px;
        color: white;
        transition: color 200ms;
        &:hover {
          color: red
        }
      }
    }
    &>.footer {
      flex-basis: 4rem;
      flex-shrink: 0;
      flex-direction: row;
      display: flex;
      align-items: center;
      justify-content: space-around;
      background-color: rgba(11, 11, 40, 1);
      border-radius: 0 0 0 30px;
      > input {
        flex-shrink: 2;
        height: 40px;
        width: 80%;
        padding-left: .25rem;
        background-color: rgba(232, 232, 232, 1);
        border-radius: 1.125rem 0 1.125rem 1.125rem;
        border-style: none;

        box-shadow:
          0 0 2rem rgba(black, 0.075),
          0rem 1rem 1rem -1rem rgba(black, 0.1);

        &:placeholder {
          color: rgba(11, 11, 40, 1);
        }
      }
      button {
        display: flex;
        flex-shrink: 1;
        border-style: none;
        align-items: center;
        height: 40px;
        font-size: 1.5rem;
        color: rgba(11, 11, 40, 1);
        cursor: pointer;
        transition: color 200ms;
        border-radius: 1.125rem 0 1.125rem 1.125rem;

        &:hover {
          background-color: rgba(11, 11, 40, 1);
          color: white;
        }
      }
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
