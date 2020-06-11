
<template>
  <div class="combination" :title="combinationsText">
    <div class="icon-wrapper">
      <img class="icon" :alt="combinationsText" :src="thumbnailIcon" />
    </div>
    <div class="desc">{{combinationsText}}</div>
    <CheckMark />
    <div class="charge">{{optionCharge}}</div>
  </div>
</template>
<style lang="scss" scoped>
@import './ImprintOption.scss';
</style>
<script>
// eslint-disable-next-line no-unused-vars
// import { mapGetters, mapActions } from 'vuex'
// import { mapGetters, mapActions } from 'vuex'
import CheckMark from '../CheckMark/CheckMark'
export default {
  components: { CheckMark },
  props: {
    combinationsText: String,
    thumbnailFilename: Number,
    callback: Function
  },
  data() {
    return {
      // thumbnailFilename1: 'CALENDAR_001.jpg'
      // // thumbnailIcon: `/assets/resources/${this.thumbnailFilename1}`
    }
  },
  computed: {
    optionCharge() {
      return '$3.5'
    },
    thumbnailIcon() {
      return require('../../assets/resources/CALENDAR_001.jpg')
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
