/* eslint-disable */
<template>
  <div v-bind:class="[{ on: checked }, 'check']" @click="say">
    <span class="mark" />
    {{message}}
  </div>
</template>

<style lang="scss" scoped>
@import './CheckMark.scss';
</style>
<script>
// eslint-disable-next-line no-unused-vars
// import { mapGetters, mapActions } from 'vuex'
export default {
  data() {
    return {
      checked: false,
      message: 'Hello'
    }
  },
  methods: {
    say() {
      this.checked = !this.checked
      this.reversedMessage()
    },
    reversedMessage() {
      // `this` points to the vm instance

      this.message = this.message
        .split('')
        .reverse()
        .join('')
    }
  }
}
</script>
