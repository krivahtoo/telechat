<template>
  <div class="message">{{ txt }}</div>
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

</style>
