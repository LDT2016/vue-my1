<template>
  <div id="counter" class="counter">
    Clicked: {{ count }} times, count is {{ evenOrOdd }}.
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
    <button @click="incrementIfOdd">Increment if odd</button>
    <button @click="incrementAsync">Increment async</button>
    <plus />
  </div>
</template>

<style scoped>
@import './../../scss/count';
</style>
<script>
// eslint-disable-next-line no-unused-vars
import { mapGetters, mapActions, mapState } from 'vuex'
import plus from '../Plus/Plus'
export default {
  data: () => {
    return {
      msg: 'My first Vue app'
    }
  },
  computed: { ...mapGetters(['evenOrOdd', 'count']) },
  // computed: {
  //   // eslint-disable-next-line
  //   evenOrOdd: function() {
  //     return this.$store.state.count
  //   }
  // },
  // eslint-disable-next-line no-undef
  // computed: mapState({
  //   // 箭头函数可使代码更简练
  //   count: state => state.count,

  //   // 传字符串参数 'count' 等同于 `state => state.count`
  //   countAlias: 'count',

  //   // 为了能够使用 `this` 获取局部状态，必须使用常规函数
  //   // eslint-disable-next-line space-before-function-paren
  //   countPlusLocalState: state => {
  //     return state.count + this.localCount
  //   }
  // }),
  methods: mapActions(['increment', 'decrement', 'incrementIfOdd', 'incrementAsync']),
  components: { plus }
}
</script>
