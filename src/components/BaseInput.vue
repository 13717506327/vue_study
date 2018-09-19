<template>
  <span>
    <input
      :value="value"
      @input="input"
      @change='change'
      v-bind="$attrs"
    >
  </span>
  
</template>

<script>
export default {
  inheritAttrs: false,
  props: ['value'],
  data () {
    return {}
  },
  methods: {
    input ($event) {
      console.log($event.target.value);
      /* 
      * this.$attrs 获取穿入组件的 属性 不包括 class
      * {placeholder: "请输入文本", type: "password"}
      */
      console.log(this.$attrs);
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
