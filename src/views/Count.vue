<template>
  <div class="count">
    <h1>This is an count page</h1>
    {{$store.state.count}}
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
  </div>
</template>

<script>
export default {
  methods: {
    // store.jsのmutasionsを呼ぶ場合はcommit、actionsを呼ぶ場合はdispatchで呼ぶ
    increment() {
      this.$store.commit("increment")
    },
    decrement() {
      this.$store.commit("decrement")
    }
  }
}
</script>
