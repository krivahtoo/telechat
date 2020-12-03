<template>
  <div class="message" :class="{incoming: incoming}">{{ txt }}</div>
</template>

<script>
export default {
  name: 'Message',
  props: {
    txt: String,
    incoming: Boolean
  }
}
</script>

<style lang="scss" scoped>
.message {
  box-sizing: content-box;
  padding: 0.5rem;
  margin: 0.5rem 1rem;
  background: #FFF;
  border-radius: 1.125rem 1.125rem 1.125rem 0;
  width: fit-content;
  max-width: 66%;

  box-shadow:
    0 0 2rem rgba(black, 0.075),
    0rem 1rem 1rem -1rem rgba(black, 0.1);

  &.incoming {
    margin: 0.5rem 1rem 0.5rem auto ;
    border-radius: 1.125rem 1.125rem 0 1.125rem;
    background: rgba(11, 11, 40, 1);
    color: white;
  }
}
</style>
