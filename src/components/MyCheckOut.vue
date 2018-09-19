<template>
  <span>
    <input
      type="checkbox"
      v-bind:checked="checked"
      v-on:change="change"
      v-bind:value="$attrs.value" 
    >
  </span>
  
</template>

<script>
export default {
  inheritAttrs: false,
  model: {
    prop: 'checked',
    event: 'change'
  },
  props: {
    checked: Boolean
  },
  data () {
    return {}
  },
  methods: {    
    change ($event) {
      this.$emit('change', $event.target.checked)
    }    
  }
}
</script>

<style lang="sass" scoped>

</style>
