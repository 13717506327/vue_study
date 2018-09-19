<template>
  <div class="v-model">
    <h1>自定义v-model</h1>
    <my-check-out v-model="myChecked" value="onona" @change="checkedChange"></my-check-out>
  </div>
</template>

<script>
import MyCheckOut from '@/components/MyCheckOut'
export default {
  components: {
    MyCheckOut
  },
  data () {
    return {
      myChecked: false
    }
  },
  methods: {
    checkedChange (value) {
      console.log('changeValue', value)
      console.log('myChecked',this.myChecked)
      console.log('input-value',document.querySelector('input').value)
    } 
  }
}
</script>

<style lang="sass" scoped>

</style>
