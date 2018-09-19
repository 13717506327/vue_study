<template>
  <input
    :value="value"
    @input="input"
    @change='change'
  >
</template>

<script>
export default {
  props: ['value'],
  data () {
    return {}
  },
  methods: {
    input ($event) {
      console.log($event.target.value)
      this.$emit('input', $event.target.value)
    },
    change ($event) {
      this.$emit('change', $event.target.value)
    }

  }
}
</script>

<style lang="sass" scoped>

</style>
